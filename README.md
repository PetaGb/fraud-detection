# fraud-detection

## key challenges:

- undocumented dataset, where meaning of many fetures would be hard to decode
- handling large amount of missing values
- handling heavily imbalanced target variable


## Likely Meaning of Each Column

| Column | Interpretation / What It Represents | Notes / Possible Nuances |
|---|---|---|
| `dpd_5_cnt` | Number of cases where the client was **5 days past due** | Present only for clients with delays (675 non-null) |
| `dpd_15_cnt` | Number of cases with **15+ days past due** | Indicates more serious delay |
| `dpd_30_cnt` | Number of cases with **30+ days past due** | Even more severe delinquency |
| `close_loans_cnt` | Count of loans that were **closed / fully repaid** | Most records have this value |
| `federal_district_nm` | Code of **federal district / region / administrative area** | Numeric code for geographic region |
| `payment_type_0` to `payment_type_5` | **One-hot encoded payment types** — e.g., type of repayment method, loan product, or payment channel | Binary indicators (0/1) for each payment type |
| `past_billings_cnt` | Number of **past billing statements** or previous credit cycles | Missing for clients without prior history |
| `score_1` | **Credit score** or risk score assigned by model 1 | Continuous variable, may contain missing values |
| `score_2` | **Alternative score** (e.g., from a second model) | Only filled for a small subset (239 non-null) |
| `age` | Client’s **age** | Integer |
| `gender` | Client’s **gender** | Encoded as integer (e.g., 0 = female, 1 = male) |
| `bad_flag` | **Target variable** — whether the client is “bad” (default / delinquent) | Usually binary: 0 = good, 1 = bad |
| `rep_loan_date_year` / `rep_loan_date_month` / `rep_loan_date_day` | **Date of loan repayment** (year, month, day) | May represent the last loan repayment or reporting date |
| `rep_loan_date_weekday` | **Day of the week** when repayment occurred | Encoded as 0–6 |
| `first_loan_year` / `first_loan_month` / `first_loan_day` | **Date of the first loan** taken by the client | Shows client’s first engagement with the lender |
| `first_loan_weekday` | **Weekday of first loan** | Useful for behavioral analysis |
| `first_overdue_date_year` / `first_overdue_date_month` / `first_overdue_date_day` | **Date of first overdue payment** | Only filled for clients with any overdue history |
| `first_overdue_date_weekday` | **Weekday of the first overdue event** | Often has values for all rows (possibly default-filled) |
