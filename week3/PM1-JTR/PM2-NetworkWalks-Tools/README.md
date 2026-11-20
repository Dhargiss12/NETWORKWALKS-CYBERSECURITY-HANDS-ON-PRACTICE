# W3-PM2: Password Cracking with Networkwalks Tools

## 1. Objective

The objective of this exercise was to perform a dictionary-based password attack using the Networkwalks Password Cracker and its associated Hash Calculator.

The lab demonstrated a browser-based password-cracking workflow using a provided PDF hash and a built-in password dictionary.

## 2. Tools Used

| Tool | Purpose |
|---|---|
| Networkwalks Password Cracker | Performs dictionary-based password testing |
| Networkwalks Hash Calculator | Used to obtain the PDF hash for the exercise |
| Built-in dictionary | Provides candidate passwords for testing |
| Web browser | Accesses the Networkwalks tools |

## 3. Practical Workflow

### Step 1: Open the Networkwalks Password Cracker

Visit:

https://networkwalks.com/password-cracker/

The tool provides a dictionary-attack interface for password recovery.

### Step 2: Extract the PDF hash

Use the Networkwalks Hash Calculator provided for the exercise to obtain the hash of the practice PDF.

The hash is then supplied to the Password Cracker.

Do not publish the complete hash of the practice file in this repository.

### Step 3: Enter the hash

Paste the extracted PDF hash into the PDF hash input field.

The interface identifies the input as a PDF password hash.

### Step 4: Select the dictionary

The built-in dictionary option was selected.

The interface displayed a built-in list containing 100 passwords.

### Step 5: Start the dictionary attack

Start the cracking process using the interface's Start Cracking control.

The tool tests candidate passwords against the supplied hash.

### Step 6: Observe the result

During the observed run, the interface displayed:

- 91 out of 100 attempts tried.
- Approximately 91% progress.
- A successful password recovery message.

The recovered password displayed by the tool was `password1`.

### Step 7: Capture the lab flag

After successful password recovery, the lab displayed a congratulations message confirming that the first flag had been captured.

The flag is retained in the original lab evidence. Avoid publishing it unless Networkwalks explicitly permits public disclosure.

## 4. Result

**Status: Successfully completed.**

- PDF password recovered.
- Built-in dictionary attack executed.
- First lab flag captured.

## 5. Key Learnings

1. Learned how to use a browser-based password-cracking tool.
2. Understood the role of a PDF password hash.
3. Practiced dictionary-based password testing.
4. Observed password-testing progress and successful recovery.
5. Compared a browser-based workflow with command-line password cracking.
6. Captured lab completion evidence.

## 6. Evidence

Add the following screenshots to the `screenshots/` directory.

| Screenshot | Description |
|---|---|
| `01-password-cracker.png` | Networkwalks Password Cracker showing the successful password recovery |
| `02-flag-captured.png` | Congratulations screen confirming the first flag was captured |

## 7. Security Takeaway

A password dictionary attack can identify weak passwords when they match entries in a candidate wordlist.

Strong, unique passwords make dictionary-based attacks less effective.

## Disclaimer

This exercise was performed using the Networkwalks educational password-cracking tool and the practice materials supplied for the lab.
