# Rust_Keylogger

CSC-1009 - 93686 - Advanced Scripting 

Report: Rust Keylogger Code and Dependencies 

Submitted by: Altamash Karlekar 

 

Code Overview 

The provided Rust code is for a keylogger, a program that records the keys pressed on a keyboard. It captures keyboard events and logs them to a file. Let's go over the important sections of the code: 

    Dependencies 

    The code relies on several external libraries, or Crates, to work correctly. These dependencies are specified in the Cargo.toml file. Here are the key dependencies: 

    getopts: Helps with command-line argument parsing. 

    env_logger: Provides logging functionality for debugging. 

    libc: Provides access to low-level C library functions. 

    log: A logging framework used in conjunction with env_logger. 

    Configuration 

    The code defines a Config structure to hold configuration settings. It includes fields for the device file (the keyboard input) and the log file (where key presses are logged). 

    Main Function 

    The main function is the entry point of the program. 

    It checks if the program is running with root privileges, as it needs such permissions to access keyboard input. 

    Initializes a logger for debugging purposes. 

    Parses command-line arguments to determine the device and log file. 

    Opens the device file and log file for reading and writing. 

    Sets up a buffer to read keyboard events. 

    Monitors keyboard input and logs key presses and releases. 

 

Root Check 

    A function called root_check checks if the program is running as the root user (administrator). If not, it terminates because it needs administrative privileges to access keyboard input. 

    Argument Parsing 

    The parse_args function uses the getopts library to parse command-line arguments. 

    It allows users to specify the device and log file as options. 

    Keyboard Device Detection 

    The get_default_device function tries to detect the keyboard device file by analyzing system information in /proc/bus/input/devices. 

    It selects the default device if only one keyboard is found; otherwise, it prompts the user to specify a device using the -d flag. 

 

Screenshots 

    Main.rs file 

 

 

 

 

    Code Run 

 

 

 

    Output file/ Keystroke Captured 

 

 

 
