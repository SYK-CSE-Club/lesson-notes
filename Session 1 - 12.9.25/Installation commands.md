# Node JS Installation
- Open Terminal
- Copy the below code by clicking on the copy button
- Paste it in the terminal window and hit enter
- Then just wait until Node JS is downloaded

```powershell
$nodeUrl="https://nodejs.org/dist/v22.19.0/node-v22.19.0-win-x64.zip"; $homeDir=$env:USERPROFILE; $zipPath=Join-Path $homeDir "node-v22.19.0-win-x64.zip"; $extractPath=$homeDir; $nodePath=Join-Path $homeDir "node-v22.19.0-win-x64"; $nodeBinPath=Join-Path $nodePath "node.exe"; Write-Host "Downloading Node.js..." -ForegroundColor Yellow; Invoke-WebRequest -Uri $nodeUrl -OutFile $zipPath -UseBasicParsing; Write-Host "Extracting..." -ForegroundColor Yellow; Expand-Archive -Path $zipPath -DestinationPath $extractPath -Force; if (Test-Path $nodeBinPath) { Remove-Item $zipPath -Force; Write-Host "Adding to PATH..." -ForegroundColor Yellow; $currentPath=[Environment]::GetEnvironmentVariable("PATH", "User"); if (-not ($currentPath -like "*$nodePath*")) { $newPath=if ($currentPath) { "$currentPath;$nodePath" } else { $nodePath }; [Environment]::SetEnvironmentVariable("PATH", $newPath, "User") }; $env:PATH += ";$nodePath"; Write-Host "✓ Node.js installed successfully!" -ForegroundColor Green; Write-Host "Location: $nodePath" -ForegroundColor Cyan; & "$nodePath\node.exe" --version } else { Write-Host "✗ Installation failed" -ForegroundColor Red }
```
## Post Installation Instructions
- Close the current terminal window
- Open a new terminal window
- Then run these commands:

```powershell
node -v
npm -v
```
**Expected output:**

```powershell
node -v
# v22.19.0
npm -v
# 10.9.3
```

- If you see these version numbers, Node.js and npm are installed successfully!
