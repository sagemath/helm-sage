# Overview
`helm-sage` provides a [helm](https://github.com/emacs-helm/helm)
 source for
[sage-shell-mode](https://github.com/stakemori/sage-shell-mode).

![helm-sage](images/helm-sage.gif)

# Installation
You will be able to install `helm-sage` from
[MELPA](https://github.com/milkypostman/melpa.git) by package.el
(`M-x package-install helm-sage`).

# An example for Setting
Bind `helm-sage-shell`,
`helm-sage-shell-describe-object-at-point` and
`helm-sage-command-history` to some keys, e.g.:
```lisp
(defun helm-sage-set-up ()
  (local-set-key (kbd "C-c C-i") 'helm-sage-shell)
  (local-set-key (kbd "C-c C-d") 'helm-sage-shell-describe-object-at-point)
  (local-set-key (kbd "M-r") 'helm-sage-command-history))
(add-hook 'sage-shell-mode-hook 'helm-sage-set-up)
```
