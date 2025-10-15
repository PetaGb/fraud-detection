# credit-risk-detection

## key challenges:

- undocumented dataset of unknown origin (possibly synthetic), meaning of many features could be hard to decode. 
- a large amount of missing values
- a heavily imbalanced target variable
- 11 columns with date values

## Likely Meaning of Each Column

| Column | Interpretation / What It Represents | 
|---|---|
| `dpd_5_cnt` | Number of cases where the client was **5 days past due** | 
| `dpd_15_cnt` | Number of cases with **15+ days past due** | 
| `dpd_30_cnt` | Number of cases with **30+ days past due** | 
| `close_loans_cnt` | Count of loans that were **closed / fully repaid** | 
| `federal_district_nm` | Code of **federal district / region / administrative area** | 
| `payment_type_0` to `payment_type_5` | **One-hot encoded payment types** | 
| `past_billings_cnt` | Number of **past billing statements** or previous credit cycles | 
| `score_1` | **Credit score** or risk score assigned by model 1 | 
| `score_2` | **Alternative score** (e.g., from a second model) | 
| `age` | Client’s **age** | 
| `gender` | Client’s **gender** |
| `bad_flag` | **Target variable** 0 = good, 1 = bad |
| `rep_loan_date_year` / `rep_loan_date_month` / `rep_loan_date_day` | **Date of loan repayment** (year, month, day) | 
| `rep_loan_date_weekday` | **Day of the week** when repayment occurred | 
| `first_loan_year` / `first_loan_month` / `first_loan_day` | **Date of the first loan**|
| `first_loan_weekday` | **Weekday of first loan** | 
| `first_overdue_date_year` / `first_overdue_date_month` / `first_overdue_date_day` | **Date of first overdue payment** |
| `first_overdue_date_weekday` | **Weekday of the first overdue event** | 
