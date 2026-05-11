# 🖥️ OS Patch Data

> Publicly available, daily-updated JSON feeds of **Windows** and **macOS** patch/release data.  
> Automatically scraped and published via GitHub Actions.

---

## 📂 Available Data Feeds

| File | Description | Raw URL |
|------|-------------|---------|
| `windows_patches.json` | Windows OS patch/update data — KB articles, OS builds, release dates | [Download](https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/windows_patches.json) |
| `macos_releases.json` | macOS release data — version numbers, build numbers, release dates | [Download](https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/macos_releases.json) |
| `os_eol_catalog.json` | End-of-life catalog for Windows and macOS operating systems | [Download](https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/os_eol_catalog.json) |

---

## ⚡ Quick Start

### cURL

```bash
# Fetch the latest Windows patch data
curl -sL https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/windows_patches.json | jq .

# Fetch the latest macOS release data
curl -sL https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/macos_releases.json | jq .

# Fetch the OS end-of-life catalog
curl -sL https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/os_eol_catalog.json | jq .
```

### PowerShell

```powershell
# Fetch the latest Windows patch data
$windows = Invoke-RestMethod -Uri "https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/windows_patches.json"
$windows | ConvertTo-Json -Depth 10

# Fetch the latest macOS release data
$macos = Invoke-RestMethod -Uri "https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/macos_releases.json"
$macos | ConvertTo-Json -Depth 10

# Fetch the OS end-of-life catalog
$eol = Invoke-RestMethod -Uri "https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/os_eol_catalog.json"
$eol | ConvertTo-Json -Depth 10
```

### Python

```python
import requests

url = "https://raw.githubusercontent.com/jr-ia/os-patch-data/main/data/windows_patches.json"
data = requests.get(url).json()
print(data)
```

---

## 🔄 Update Schedule

This data is refreshed **daily at 7:00 PM UTC** via GitHub Actions.

> **Note:** Actual data changes only occur when Microsoft or Apple publish new OS releases or patches. On days with no upstream changes, no new commit is created.

You can track the commit history of this repo to see exactly when data last changed.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, and distribute.

---

## 🤝 Contributing

This is an automated data feed. The source scraper lives in a private repository.

- **Found an issue with the data?** Open a [GitHub Issue](https://github.com/jr-ia/os-patch-data/issues).
- **Have a suggestion or feature request?** Issues and PRs for the README, documentation, or data format improvements are welcome.
