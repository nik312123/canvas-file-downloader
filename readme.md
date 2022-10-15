# Canvas File Downloader

Simple file downloader for Canvas of Instructure.

Features:

- Downloads all courses or only the ones marked as favorites
- Download from modules, files, submissions, or all
- If a file already exists, it's omitted
- If a Google Drive file is linked, it will be downloaded

Usage:

First, download the requirements with:

```shell
python -m pip install -r requirements.txt
```

then, run the module with:

```shell
python canvas.py YOUR-TOKEN CANVAS-DOMAIN USER-ID
```

Where:

- `YOUR-TOKEN`: The access token from Canvas. This can be created by going to Canvas and navigating to `Account` > `Settings` > `Approved Integrations` > `New Access Token`.
- `CANVAS-DOMAIN`: the Canvas domain from which the files will be downloaded (**without** http:// or https://). For example, `example.instructure.com`.
- `USER-ID`: your Canvas user ID. This can be found at `https://example.instructure.com/api/v1/users/self` in the `id` field, assuming that you replace `example.instructure.com` with `CANVAS-DOMAIN`.

Optional parameters:

- `-f FROM`: where to download the files, can be modules,
  folders or both (default: `both`).
- `-o DIR`: name of the output directory (default: `CanvasFiles`).
- `--all`: include all courses instead of only favorites.

Related projects:

- [CanvasSync](https://github.com/perslev/CanvasSync)
- [CanvasAPI](https://github.com/ucfopen/canvasapi)
- [Canvas LMS](https://github.com/instructure/canvas-lms)

[get_token]: https://cursos.canvas.uc.cl/profile/settings#access_tokens
