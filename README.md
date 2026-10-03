# banana-leaf-media

Public image host for **approved** Banana Leaf Restaurant Instagram posts.

Instagram's API fetches images from a public URL, so each approved image is committed here and
served from `https://raw.githubusercontent.com/<owner>/banana-leaf-media/main/posts/<YYYY-MM>/<random>.jpg`.

- Files are added only by `banana-leaf-social/scripts/post.py`. Don't add files by hand.
- Filenames are random (128-bit) so unpublished images can't be guessed.
- Images are re-encoded JPEGs with all metadata (EXIF/GPS) removed.
- `.gitignore` blocks everything except `posts/**/*.jpg` and these repo files, so nothing else
  (and no credentials) can be pushed by accident.
