
# Ubuntu Basic Commands

This guide provides a list of essential commands for navigating and managing Ubuntu systems. These commands are fundamental for performing basic tasks in the terminal.

## Navigation Commands

- **`pwd`**: Print the current working directory.
  ```bash
  pwd
  ```

- **`ls`**: List directory contents.
  ```bash
  ls
  ```

- **`cd [directory]`**: Change the current directory to `[directory]`.
  ```bash
  cd /path/to/directory
  ```

- **`cd ..`**: Move up one directory level.
  ```bash
  cd ..
  ```

## File and Directory Management

- **`touch [file]`**: Create a new empty file named `[file]`.
  ```bash
  touch newfile.txt
  ```

- **`mkdir [directory]`**: Create a new directory named `[directory]`.
  ```bash
  mkdir new_directory
  ```

- **`cp [source] [destination]`**: Copy files or directories.
  ```bash
  cp source.txt destination.txt
  ```

- **`mv [source] [destination]`**: Move or rename files or directories.
  ```bash
  mv oldname.txt newname.txt
  ```

- **`rm [file]`**: Remove a file.
  ```bash
  rm unwantedfile.txt
  ```

- **`rm -r [directory]`**: Remove a directory and its contents.
  ```bash
  rm -r old_directory
  ```

## File Viewing and Editing

- **`cat [file]`**: Display the contents of a file.
  ```bash
  cat filename.txt
  ```

- **`nano [file]`**: Edit a file using the Nano text editor.
  ```bash
  nano filename.txt
  ```

- **`less [file]`**: View the contents of a file one page at a time.
  ```bash
  less filename.txt
  ```

## System Information

- **`df -h`**: Display disk space usage in a human-readable format.
  ```bash
  df -h
  ```

- **`free -h`**: Display memory usage in a human-readable format.
  ```bash
  free -h
  ```

- **`uname -a`**: Display detailed information about the system.
  ```bash
  uname -a
  ```

## Process Management

- **`ps aux`**: List all running processes.
  ```bash
  ps aux
  ```

- **`top`**: Display active processes and system usage in real-time.
  ```bash
  top
  ```

- **`kill [PID]`**: Terminate a process by its PID (Process ID).
  ```bash
  kill 1234
  ```

- **`killall [process_name]`**: Terminate all processes with the specified name.
  ```bash
  killall processname
  ```

## Network Commands

- **`ping [hostname]`**: Check the network connection to a host.
  ```bash
  ping example.com
  ```

- **`ifconfig`**: Display network interface configuration.
  ```bash
  ifconfig
  ```

- **`netstat -tuln`**: List all listening ports.
  ```bash
  netstat -tuln
  ```

## Package Management (APT)

- **`sudo apt update`**: Update the list of available packages.
  ```bash
  sudo apt update
  ```

- **`sudo apt upgrade`**: Upgrade all installed packages to their latest versions.
  ```bash
  sudo apt upgrade
  ```

- **`sudo apt install [package]`**: Install a new package.
  ```bash
  sudo apt install package_name
  ```

- **`sudo apt remove [package]`**: Remove an installed package.
  ```bash
  sudo apt remove package_name
  ```

## Permissions and Ownership

- **`chmod [options] [file]`**: Change file permissions.
  ```bash
  chmod 755 script.sh
  ```

- **`chown [owner]:[group] [file]`**: Change file owner and group.
  ```bash
  chown user:group file.txt
  ```

## Searching and Finding Files

- **`find [directory] -name [pattern]`**: Find files matching a pattern.
  ```bash
  find /home -name "*.txt"
  ```

- **`grep [pattern] [file]`**: Search for a pattern within a file.
  ```bash
  grep "search_term" file.txt
  ```

## Helpful Shortcuts

- **`Ctrl + C`**: Cancel the current command.
- **`Ctrl + Z`**: Suspend the current process.
- **`Ctrl + L`**: Clear the terminal screen.
- **`Ctrl + R`**: Search the command history.

## Conclusion

These commands provide a solid foundation for using Ubuntu's command-line interface. For more advanced usage, consult the man pages for each command (`man [command]`), or explore additional resources and documentation.
