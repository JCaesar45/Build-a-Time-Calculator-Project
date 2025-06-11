```markdown
# Time Calculator - add_time Function

## Overview
The `add_time` function calculates the new time after adding a given duration to a start time, optionally considering a starting day of the week. It handles 12-hour clock formats, converts to 24-hour for calculations, and formats the output with appropriate annotations such as `(next day)` or `(n days later)`.

---

## Features
- Adds durations (hours and minutes) to a start time in 12-hour format.
- Handles AM/PM conversions.
- Calculates the number of days passed.
- Optionally considers the starting day of the week and computes the resulting day.
- Formats output with proper spacing, punctuation, and annotations.

---

## Usage

```python
def add_time(start, duration, starting_day=None):
    # Implementation here
``

### Parameters:
- `start` (str): The start time in `'H:MM AM/PM'` format.
- `duration` (str): The duration to add in `'H:MM'` format.
- `starting_day` (str, optional): The starting day of the week (case-insensitive).

### Returns:
- (str): The resulting time after adding the duration, formatted according to the specifications.

---

## Examples

```python
print(add_time('3:00 PM', '3:10'))
# Output: 6:10 PM

print(add_time('11:30 AM', '2:32', 'Monday'))
# Output: 2:02 PM, Monday

print(add_time('11:43 AM', '00:20'))
# Output: 12:03 PM

print(add_time('10:10 PM', '3:30'))
# Output: 1:40 AM (next day)

print(add_time('11:43 PM', '24:20', 'tueSday'))
# Output: 12:03 AM, Thursday (2 days later)

print(add_time('6:30 PM', '205:12'))
# Output: 7:42 AM (9 days later)
``

---

## Implementation Details
- Converts start time to 24-hour format for easy arithmetic.
- Adds the duration to the start time, managing minutes overflow.
- Calculates how many days have passed.
- Converts back to 12-hour format with correct AM/PM.
- Adjusts the day of the week if provided.
- Formats the output string with all relevant annotations.

---

## Notes
- The function assumes valid input times.
- Minutes in duration are integers less than 60.
- Hours in duration can be any whole number.
- No external libraries are used.

---

## License
This project is for educational purposes. Feel free to modify and extend!

---

## Contact
For questions or contributions, contact Jordan Leturgez at jordanleturgez@gmail.com.
```
