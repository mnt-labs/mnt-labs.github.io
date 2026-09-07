# The file digest

Every export shows a SHA-256 digest next to its download. It is the hash of
the exact bytes of the file you downloaded, computed when the file was
assembled. Anyone holding the file can recompute it and compare.

**macOS or Linux**

```
shasum -a 256 change-record-export.xlsx
```

**Windows (PowerShell)**

```
Get-FileHash change-record-export.xlsx -Algorithm SHA256
```

**Windows (Command Prompt)**

```
certutil -hashfile change-record-export.xlsx SHA256
```

If the printed value equals the one the app shows, the file is the one the
app produced and has not been altered since. If it differs, the file was
changed after download (or is a different export).

The digest is also stored with the export job inside the app, so the
comparison can be made later without the original browser session. For an
XLSX, the "Export settings" sheet inside the file states what produced it;
the digest covers that sheet too.
