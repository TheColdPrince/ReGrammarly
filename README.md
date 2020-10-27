[![Build Status](https://travis-ci.com/jcs-elpa/grammarly.svg?branch=master)](https://travis-ci.com/jcs-elpa/grammarly)
[![MELPA](https://melpa.org/packages/grammarly-badge.svg)](https://melpa.org/#/grammarly)
[![MELPA Stable](https://stable.melpa.org/packages/grammarly-badge.svg)](https://stable.melpa.org/#/grammarly)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

# <a href="https://app.grammarly.com/"><img src="./etc/logo.png" width="40" height="40"></a> grammarly
> Grammarly API interface.

## Examples

Below is an simple example that how you can use this library for calling 
Grammarly API interface.

```el
(require 'grammarly)

(defun test-on-message (data)
  "On message callback with DATA."
  (message "[DATA] %s" data))

;; Set callback for receiving data.
(add-to-list 'grammarly-on-message-function-list 'test-on-message)

;; Send check text request.
(grammarly-check-text "Hello World")
```

## References

* [grammarly-api](https://github.com/dexterleng/grammarly-api)
* [reverse-engineered-grammarly-api](https://github.com/c0nn3r/reverse-engineered-grammarly-api)

## Todo List

- [ ] Support multiple requests at the same time.
- [ ] Support login and premium account.

## Contribution

If you would like to contribute to this project, you may either
clone and make pull requests to this repository. Or you can
clone the project and establish your own branch of this tool.
Any methods are welcome!
