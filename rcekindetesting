# rce_test.py
import os
import subprocess

def main():
    # Print environment variables to a file
    with open("env_vars.txt", "w") as f:
        for key, value in os.environ.items():
            f.write(f"{key}={value}\n")
    
    # Run 'whoami' command and write output to a file
    try:
        whoami_output = subprocess.check_output("whoami", shell=True).decode().strip()
        with open("whoami.txt", "w") as f:
            f.write(f"User: {whoami_output}\n")
    except Exception as e:
        with open("whoami_error.txt", "w") as f:
            f.write(f"Error running 'whoami': {str(e)}\n")
    
    # Run 'ls' command and write output to a file
    try:
        ls_output = subprocess.check_output("ls", shell=True).decode().strip()
        with open("ls_output.txt", "w") as f:
            f.write(f"Directory Contents:\n{ls_output}\n")
    except Exception as e:
        with open("ls_error.txt", "w") as f:
            f.write(f"Error running 'ls': {str(e)}\n")

if __name__ == "__main__":
    main()
