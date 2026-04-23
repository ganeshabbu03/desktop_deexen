# How to restore the Windows Application

The application build was split into parts to comply with GitHub's 100MB file size limit.

To restore the original `Deexen-Windows.zip` file, follow these steps:

### Windows (PowerShell)
```powershell
Get-Content Deexen-Windows.zip.part-* -ReadCount 0 | Set-Content Deexen-Windows.zip -Encoding Byte
```

### Linux / macOS (Terminal)
```bash
cat Deexen-Windows.zip.part-* > Deexen-Windows.zip
```

After running the command, you can extract `Deexen-Windows.zip` to get the `win-unpacked` directory containing the executable.
