# Overview
`helm-sage` provides a [helm](https://github.com/emacs-helm/helm)
 source for
[sage-shell-mode](https://github.com/stakemori/sage-shell-mode).

![helm-sage](images/helm-sage.gif)

# Installation
You will be able to install `helm-sage` from
[MELPA](https://github.com/milkypostman/melpa.git) by package.el
(`M-x package-install helm-sage`).

# Commands
`helm-sage` provides 3 commands, `helm-sage-shell`,
`helm-sage-shell-describe-object-at-point` and
`helm-sage-command-history`.

| Command                                  | Description                                                            |
|------------------------------------------|------------------------------------------------------------------------|
| helm-sage-shell                          | Show completions at point.                                             |
| helm-sage-shell-describe-object-at-point | Almost same as `helm-sage-shell`. But the default action is different. |
| helm-sage-command-history                | Show command history.                                                  |

In `helm-sage-shell`, press `TAB` to show the list of actions.
There are 3 actions, "Insert", "View Docstring" and "View Source File".


# An example for setting
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
