# Height Meter Feature Requirements

## Feature Description

The Height Meter feature is a system that allows users to record and track height measurements along with personal information. The feature captures individual demographic data and height measurements for analysis and reference.

## Data Fields

The height-meter feature must capture and store the following information:

- **Name**: User's full name (string)
- **Age**: User's age in years (integer)
- **Gender**: User's gender (string/enum: Male, Female, Other)
- **Height**: Height measurement in centimeters (float/decimal)

## System Reference Table

The following dummy table serves as a system reference for height statistics by age and gender:

| Age | Male (cm) | Female (cm) |
|-----|-----------|-------------|
| 1   | 70 - 85   | 65 - 82     |
| 2   | 80 - 97   | 75 - 95     |
| 3   | 85 - 100  | 80 - 100    |
| 4   | 90 -115   | 85 - 115    |
| 5   | 100 - 120 | 90 - 120    |
| 6   | 105 - 125 | 95 - 125    |
| 7   | 110 - 140 | 100 - 135   |
| 8   | 115 - 145 | 110 -  140  |
| 9   | 120 -150  | 115 - 145   |
| 10  | 125 - 155 | 120 - 150   |
| 11  | 130 - 160 | 125 - 155   |
| 12  | 135 - 165 | 130 - 155   |

*Note: Values are approximate average heights in centimeters for reference purposes.*

## Functional Requirements

1. **Data Entry**
   - System must allow users to input name, age, gender, and height
   - Age must be a positive integer
   - Height must be a positive number (in centimeters)
   - Gender selection must be provided (Male, Female, Other)

2. **Data Storage**
   - All entered data must be stored persistently
   - Data should be retrievable for future reference

3. **Data Validation**
   - Validate that all required fields are filled
   - Validate age range (e.g., 0-120 years)
   - Validate height range (e.g., 30-250 cm)

4. **Reference Comparison**
   - System should be able to compare entered height against the reference table
   - Display comparison results based on age and gender

## Technical Requirements

- Data model should support the four core fields: name, age, gender, height
- Reference table should be accessible for statistical comparisons
- System should handle data persistence (database or file storage)

