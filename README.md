# Grocery Data Processor

This project is designed to process grocery data from the `grocery_data.csv` file.


## Getting started

1. Create a venv using the VS Code "Python: Create Environments" command in the command palette
2. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

## Additional Information

Here are some useful pytest args which might help you approach this:

### Docs on the new config style:

Here are the following configurable options:
```
"python.configs": [
        {
            "name": "config unittest 1", // required and must be unique
            "type": "test", // required
            "subtype": [ // required
                "testRun",
                "testDebug",
                "testDiscovery"
            ],
            "args": ["-p", "test*.py"], // required, leave array empty if no args needed
            "env": {"PYTHONPATH": "xyz"}, // optional
            "envFile": "path/to/file", // optional
            "framework": "pytest", // required
        },
        {
            "name": "basic config with custom arg",
            "type": "test",
            "subtype": [
                "testDiscovery"
            ],
            "args": ["-vv"],
        },
        {
            "name": "debug config",
            "type": "terminal",
            "subtype": [
                "terminalRun",
                "terminalDebug"
            ],
        }
    ],
```

### Useful pytest Command-Line Arguments

1. **`-s` / `--capture=no`**
   - **Description**: Disables output capturing. This allows you to see print statements and logs directly in the terminal, regardless of whether the tests pass or fail.

2. **`-v` / `--verbose`**
   - **Description**: Increases verbosity. This option provides more detailed information about each test that is run, including a list of all tests executed.

3. **`-q` / `--quiet`**
   - **Description**: Reduces output verbosity. This option provides less detailed output, showing only summary information about the test run.

4. **`--maxfail=num`**
   - **Description**: Stops the test run after a specified number of failures. Useful for quickly identifying issues without running the entire test suite.

5. **`--tb=style`**
   - **Description**: Controls traceback print mode. Styles include `auto`, `long`, `short`, `line`, and `native`. This helps in customizing the traceback format for easier debugging.

6. **`-k expr`**
   - **Description**: Runs tests that match the given expression. Useful for selectively running tests based on part of the test name or marker.

7. **`-m marker`**
   - **Description**: Runs tests that are marked with the given marker. This is useful for organizing and selecting specific groups of tests to run.

8. **`--disable-warnings`**
   - **Description**: Disables warnings summary. This can help in reducing clutter in the test output, especially when dealing with a lot of deprecation warnings.

9. **`--durations=num`**
   - **Description**: Shows the slowest `num` tests at the end of the test run. Useful for identifying performance bottlenecks in your test suite.

10. **`--cov`**
    - **Description**: Measures code coverage using the `pytest-cov` plugin. It provides a report on how much of your code is covered by tests, helping you ensure comprehensive test coverage.

