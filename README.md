# notes
just a note mates
pdate 2026-01-13
cd "D:\Git\notes"

if (-not (Test-Path ".\activity-log.md")) {
  "# Activity Log" | Out-File -Encoding utf8 ".\activity-log.md"
}

Add-Content ".\activity-log.md" "$(Get-Date -Format 'yyyy-MM-dd HH:mm:ss') monthly check-in"

git add activity-log.md
git commit -m "Monthly check-in"
git push
