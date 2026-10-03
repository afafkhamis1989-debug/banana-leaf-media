# banana-leaf-media

Public media host (images and videos) for **approved** Banana Leaf Restaurant Instagram posts.

Instagram's API fetches media from a public URL, so each approved file is committed here and served
from GitHub Pages (`https://<owner>.github.io/banana-leaf-media/posts/<YYYY-MM>/<random>.jpg|.mp4`).
Pages serves videos as `video/mp4`; raw.githubusercontent.com serves them as `application/octet-stream`.
`.nojekyll` makes Pages serve files as-is.

- Files are added only by `banana-leaf-social/scripts/post.py`. Don't add files by hand.
- Filenames are random (128-bit) so unpublished images can't be guessed.
- Images are re-encoded JPEGs and videos re-encoded MP4s, with metadata (EXIF/GPS) removed.
- `.gitignore` blocks everything except `posts/**/*.jpg`, `posts/**/*.mp4` and these repo files, so nothing else
  (and no credentials) can be pushed by accident.
