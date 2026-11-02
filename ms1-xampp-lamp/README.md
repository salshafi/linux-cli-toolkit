# Milestone 1 - XAMPP / LAMP on Ubuntu

The goal was to get a working web server with PHP running and confirm it by loading pages in the browser.

## What I did

1. Installed XAMPP on Ubuntu and started Apache from the XAMPP control script.
2. Put my files in the `htdocs` folder (that's the folder Apache serves).
3. Opened `http://localhost/introEx.php` to check PHP was running.
4. Opened `http://localhost/form.html`, filled in a name and email, and submitted. That sends a POST request to `welcome.php`, which prints the values back.

## Screenshots

XAMPP control panel with Apache, MySQL and ProFTPD running:

![XAMPP running](1a-xampp-manager-running.png)

Project files created in the htdocs folder:

![project files](3-project-files-created.png)

`introEx.php` in the browser:

![introEx.php output](3-introEx.png)

The form filled in:

![form filled in](5-form-filled.png)

The result after submitting:

![welcome.php result](6-welcome-result.png)

The source of the three files (`cat` in the terminal):

![source code](8-source-code-verification.png)
## Files

| File | What it does |
|------|--------------|
| `introEx.php` | Prints one line to confirm PHP works |
| `form.html` | Simple form with name and email fields, posts to `welcome.php` |
| `welcome.php` | Reads the two values from `$_POST` and echoes them |

## Notes

- `welcome.php` prints whatever the user typed straight back out. That is fine for a class exercise, but in anything real the values should be escaped first (for example with `htmlspecialchars()`), otherwise someone could put HTML or script in the name field. I haven't added that here because I wanted to keep the file as I submitted it.
- There is also no check for empty fields.
