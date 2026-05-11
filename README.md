# AutoWD Panel QQ

Bot withdrawal otomatis via myBCA + panel web.

## Link Panel
**https://okto88-alt.github.io/autowdQQ/panel_qq.html**

## Setup Staff (sekali saja)

1. Download `agent.exe` + `adb.exe` + `AdbWinApi.dll` + `AdbWinUsbApi.dll`
2. Taruh semua dalam 1 folder
3. Jalankan `agent.exe` — catat IP yang tampil di console
4. Buka browser → link panel di atas
5. Masukkan `ws://[IP-PC]:8765` → Connect

## Update Resource-id (kalau myBCA update)

Edit `config/xpath_qq.json` di GitHub repo ini.
Agent akan otomatis fetch config terbaru saat start berikutnya.
Tidak perlu install ulang apapun di PC staff.

## Struktur Repo

```
panel_qq.html      ← panel web (GitHub Pages)
config/
└── xpath_qq.json  ← resource-id myBCA (edit di sini kalau update)
README.md
```

## Struktur Folder Agent (PC Staff)

```
agent.exe          ← jalankan ini
adb.exe
AdbWinApi.dll
AdbWinUsbApi.dll
```

File lain (config, queue, screenshot) dibuat otomatis saat pertama jalan.

## Build agent.exe (untuk developer)

```bash
pip install -r requirements.txt
pyinstaller --onefile --name agent agent.py
```
