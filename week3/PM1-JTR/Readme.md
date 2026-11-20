# W3-PM1: Password Cracking with John the Ripper

## 1. Objective

The objective of this exercise was to recover the password of a password-protected PDF using John the Ripper (JTR) and a dictionary-based attack.

The exercise involved extracting the PDF password hash, preparing the required environment, and testing candidate passwords from a wordlist.

## 2. Tools Used

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| pdf2john | Extracts password hash information from a PDF |
| John the Ripper | Performs password recovery attempts |
| pyHanko | Required PDF processing dependency in this environment |
| Python virtual environment | Isolates Python dependencies |
| RockYou | Dictionary wordlist |

## 3. Lab Environment

- Operating System: Kali Linux 2026.3
- Virtualization: Oracle VirtualBox
- Target file: `My-Locked-PDF1.pdf`
- Hash output: `~/hash.txt`
- Wordlist: `/usr/share/wordlists/rockyou.txt`

## 4. Practical Workflow

### Step 1: Locate the target PDF

The practice PDF was stored in the VirtualBox shared folder.

```bash
cd /media/sf_Windows_Share
```

Identify the file:

```bash
file My-Locked-PDF1.pdf
```

The file command was used to identify the file type.

### Step 2: Prepare the Python environment

A separate Python virtual environment was created for the required PDF dependency.

```bash
python3 -m venv ~/pdf-env
```

Activate the environment:

```bash
source ~/pdf-env/bin/activate
```

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

Install pyHanko:

```bash
python -m pip install pyHanko
```

Verify the installation:

```bash
python -m pip show pyHanko
```

The installed version observed during the lab was 0.38.2.

### Step 3: Extract the PDF hash

The `pdf2john` utility was used to extract the password hash from the provided PDF.

```bash
pdf2john My-Locked-PDF1.pdf > ~/hash.txt
```

The extracted hash was saved in the home directory because the VirtualBox shared folder did not allow writing.

Verify that the hash file contains data:

```bash
wc -c ~/hash.txt
```

**Observed output:** 193 bytes.

The hash was inspected using:

```bash
cat ~/hash.txt
```

The extracted hash is not included in this public documentation.

### Step 4: Prepare the wordlist

The RockYou wordlist was available at:

```text
/usr/share/wordlists/rockyou.txt
```

If the wordlist is still compressed, it can be extracted with:

```bash
sudo gzip -dk /usr/share/wordlists/rockyou.txt.gz
```

The `-d` option decompresses the file, while `-k` keeps the original compressed file.

### Step 5: Run John the Ripper

The following command performs a dictionary attack against the extracted PDF hash:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt ~/hash.txt
```

**Explanation:**

- `john`: Starts John the Ripper.
- `--wordlist`: Specifies the dictionary file.
- `/usr/share/wordlists/rockyou.txt`: The candidate password list.
- `~/hash.txt`: The extracted PDF hash file.

John the Ripper tested candidate passwords against the extracted hash.

### Step 6: Verify the recovered password

Use the following command to display the recovered result:

```bash
john --show --format=PDF ~/hash.txt
```

This is the recommended verification command. Run it if you have not yet captured its output.

## 5. Result

**Status: Password recovered successfully.**

The John the Ripper output showed:

- One PDF password hash loaded.
- One password hash successfully recovered.
- The cracking session completed.

The recovered password was `password1`.

The password is recorded here for the educational lab result; it should not be reused as a real account password.

## 6. Key Learnings

1. Learned how to identify a PDF file in Linux.
2. Understood the purpose of PDF password hash extraction.
3. Installed Python dependencies in an isolated virtual environment.
4. Learned how to use a dictionary wordlist with John the Ripper.
5. Understood how to verify recovered password results.
6. Practiced handling file permissions in a VirtualBox shared folder.

## 7. Evidence

Add your screenshots to the `screenshots/` directory.

| Screenshot | Description |
|---|---|
| `01-pdf-hash-extraction.png` | Shows the PDF hash extraction and hash file verification |
| `02-john-cracking-result.png` | Shows the John the Ripper result |

## 8. Security Takeaway

Dictionary attacks demonstrate why common and predictable passwords are weak.

Using unique, long passwords and a password manager helps reduce the risk of successful dictionary-based password attacks.

## Disclaimer

This exercise was performed on a practice PDF supplied for an authorized Networkwalks educational lab.
