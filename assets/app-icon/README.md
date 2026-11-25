# Patronus PDF app icon

The Patronus shield with a "P", in red for Patronus PDF (green for Patronus Design, blue for Patronus
Photo, silver for the Patronus Launcher), on a dark rounded tile so that it reads on light and dark
backgrounds. `patronuspdf-document.*` is the separate icon for PDF files opened with the app.

`source/patronus-pdf-shield.png` is the transparent shield master. The app-icon files in this
directory (`patronuspdf-1024.png`, `patronuspdf.ico`, `patronuspdf.icns`, `patronuspdf.svg`,
`patronuspdf-small.svg` and `hicolor/`) are generated from it by `packaging/make-icons.py` (needs
Pillow) and are committed, so builds never need Pillow:

```
python3 packaging/make-icons.py assets/app-icon/source/patronus-pdf-shield.png assets/app-icon patronuspdf com.patronus.patronuspdf
```

The master was cut from the logo supplied by the project owner, so its resolution is limited: a
vector original would give sharper large sizes.
