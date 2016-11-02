---
layout: post
category : emacs
---
Write some PowerShell code in any Emacs buffer.

Select it, then `M-x eval-region-powershell` to evaluate as a PowerShell script block. The output goes into `*Shell Command Output*`.

Update: Much improved thanks to a comment by [TarMil](http://www.reddit.com/r/emacs/comments/1d5rlt/evaluate_the_active_region_in_emacs_using/)

    (defun eval-region-powershell ()
      (interactive)
      (shell-command
       (concat "powershell -noprofile -encodedcommand "
               (base64-encode-string
                (encode-coding-string (buffer-substring (mark) (point)) 'utf-16le)))))
