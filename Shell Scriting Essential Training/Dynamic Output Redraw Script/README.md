To create a Linux Bash script that updates its output each time the result changes, you can use a combination of a loop, conditional checks, and the `tput` command to redraw the output on the terminal. Here's an example script:

### Script: `dynamic_output.sh`

```bash
#!/bin/bash

# Initial result placeholder
previous_result=""

# Infinite loop
while true; do
    # Command to fetch the result (e.g., `date` for dynamic output)
    current_result=$(date +%H:%M:%S)

    # Check if the result has changed
    if [[ "$current_result" != "$previous_result" ]]; then
        # Clear the terminal line and redraw the output
        tput cuu1 && tput el
        echo "Current Time: $current_result"

        # Update the previous result
        previous_result="$current_result"
    fi

    # Sleep for a short duration to reduce CPU usage
    sleep 1
done
```

### How It Works:
1. **Command Execution**: Replace `date +%H:%M:%S` with the command or logic that generates the output you want to monitor.
2. **Change Detection**: The script compares the `current_result` with `previous_result`. If they differ, it redraws the output.
3. **Redrawing**: The `tput cuu1` moves the cursor up one line, and `tput el` clears the line before printing the new output.
4. **Infinite Loop**: It continuously checks for changes and updates the output as needed.
5. **Sleep**: Introduces a delay to avoid excessive CPU usage.

### Run the Script
Make the script executable and run it:
```bash
chmod +x dynamic_output.sh
./dynamic_output.sh
```

You can modify the script to suit your specific use case by changing the `current_result` assignment. For example, you can monitor file changes, system stats, or the output of a specific command.