# NEOS notifications
[![Latest Stable Version](https://poser.pugx.org/breadlesscode/neos-notification/v/stable)]()
[![Downloads](https://img.shields.io/packagist/dt/breadlesscode/neos-notification.svg)]()
[![license](https://img.shields.io/github/license/breadlesscode/neos-notification.svg)]()

This package includes a notification compoment and a notification node type for the backend.

## Installation
```
composer require breadlesscode\notification
```
## Configuration
```yaml
Breadlesscode:
  Notification:
    classes:
      base: 'alert' # if you only set base class, BEM naming is used
      content: 'alert-content'
      info: 'alert-info'
      warning: 'alert-warning'
      danger: 'alert-danger'
```
## Usage
You can use the component like this in fusion:
```
    notification = Breadlesscode.Components:Notification {
        onlyRenderInBackend = ${ false }
        type = 'info'
        content 'Hello world'
        # and you can override the class configuration
        baseClass = 'notification' # for BEM naming
        contentClass = 'notification__content'
        containerClass = 'notification'
    }
```
