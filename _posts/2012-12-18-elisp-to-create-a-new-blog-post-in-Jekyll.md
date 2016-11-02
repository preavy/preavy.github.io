---
layout: post
category : tech
---

Here's some cheap and cheerful elisp to start a new blog post in Jekyll.

    (defun new-post (title)
      "Start a new blog post"
      (setq path "~/path/to/_posts/")
      (interactive "sTitle: ")
      (find-file (concat path (format-time-string "%Y-%m-%d")
        "-" (replace-regexp-in-string " " "-" title) ".md"))
      (insert "---
    layout: post
    category : nil
    tags : []
    ---
    ")
    )

Just prompts you for a post title. Replaces spaces with hyphens, opens the file and inserts the YAML front matter.
