Here's a README file for your script that you can include on GitHub:

---

# Error Search Script

## Description

This Python script is designed to search for specific error messages in a log file and output matching errors to a new log file. It allows users to search for errors based on user-provided patterns and generates a file listing all occurrences of those errors.

## Features

- Searches a log file for lines containing a specified error pattern.
- Allows users to input error patterns interactively.
- Outputs the found errors to a new log file named `errors_found.log` in the user's home directory.

## Requirements

- Python 3.x
- The script should be made executable before running.

## Usage

1. **Make the script executable:**

   ```bash
   sudo chmod +x find_error.py
   ```

2. **Run the script by passing the path to your log file as a parameter:**

   ```bash
   ./find_error.py ~/data/fishy.log
   ```

3. **Enter the error pattern to search for when prompted. For example:**

   ```
   CRON ERROR Failed to start
   ```

4. **After execution, the script will generate a file named `errors_found.log` in the `~/data` directory containing all the lines that match the search pattern.**

5. **You can view the generated errors with:**

   ```bash
   cat ~/data/errors_found.log
   ```

## Example

Given a log file `fishy.log` with the following content:

```
July 31 04:11:32 mycomputername CRON[51253]: ERROR: Failed to start CRON job due to script syntax error. Inform the CRON job owner!
```

Running the script with the error pattern `CRON ERROR Failed to start` will result in `errors_found.log` containing:

```
July 31 04:11:32 mycomputername CRON[51253]: ERROR: Failed to start CRON job due to script syntax error. Inform the CRON job owner!
```

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to modify or expand on this as needed!
