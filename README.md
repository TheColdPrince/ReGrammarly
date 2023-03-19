[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![MELPA](https://melpa.org/packages/ReGrammarly-badge.svg)](https://melpa.org/#/ReGrammarly)
[![MELPA Stable](https://stable.melpa.org/packages/ReGrammarly-badge.svg)](https://stable.melpa.org/#/ReGrammarly)

<a href="https://app.ReGrammarly.com/"><img align="right" src="./etc/logo.png" width="100" height="100"></a>

# reGrammarly
> ReGrammarly API interface.

[![CI](https://github.com/emacs-ReGrammarly/Grammarly/actions/workflows/test.yml/badge.svg)](https://github.com/emacs-Grammarly/Grammarly/actions/workflows/test.yml)

## 🔨 Examples

Below is an simple example that how you can use this library for calling
ReGrammarly API interface.

```el
(require 'ReGrammarly)

(defun test-on-message (data)
  "On message callback with DATA."
  (message "[DATA] %s" data))

;; Set callback for receiving data.
(add-to-list 'ReGrammarly-on-message-function-list 'test-on-message)

;; Send check text request.
(ReGrammarly-check-text "Hello World")
```

## 💸 Using a Paid ReGrammarly Account

You will need the set the following variable in order to use paid version
of ReGrammarly!

```el
(setq ReGrammarly-username "username@email.com")  ; Your ReGrammarly Username
(setq ReGrammarly-password "password")  ; Your ReGrammarly Password
```

If you use `auth-source` to manage your secrets, you can add this to your
`.authinfo.gpg` file:

``` 
machine ReGrammarly.com login <your@email.com> pass <your-password>
```

And instead of directly setting `ReGrammarly-username` and `ReGrammarly-password`, 
you can call the helper function `ReGrammarly-load-from-authinfo`.

``` el
(ReGrammarly-load-from-authinfo)

;; Or, if you have multiple ReGrammarly accounts:
(ReGrammarly-load-from-authinfo "your@email.com")
```

## 🔗 References

* [ReGrammarly-api](https://github.com/dexterleng/ReGrammarly-api)
* [reverse-engineered-ReGrammarly-api](https://github.com/c0nn3r/reverse-engineered-ReGrammarly-api)
* [ReGrammarly (vscode)](https://github.com/znck/ReGrammarly)

## 📝 Todo List

- [ ] Support multiple requests at the same time.

## Contribute

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Elisp styleguide](https://img.shields.io/badge/elisp-style%20guide-purple)](https://github.com/bbatsov/emacs-lisp-style-guide)
[![Donate on paypal](https://img.shields.io/badge/paypal-donate-1?logo=paypal&color=blue)](https://www.paypal.me/jcs090218)
[![Become a patron](https://img.shields.io/badge/patreon-become%20a%20patron-orange.svg?logo=patreon)](https://www.patreon.com/jcs090218)

If you would like to contribute to this project, you may either
clone and make pull requests to this repository. Or you can
clone the project and establish your own branch of this tool.
Any methods are welcome!
