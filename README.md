# auth0-Lock-DOM-Customization
How to manipulate the DOM in the [Auth0 Lock](https://auth0.com/docs/libraries/lock/v11) hosted login page.

### How:
1. Copy and paste the HTML to your [Hosted login page](https://manage.auth0.com/#/login_page) configuration.
2. Insert custom text into the login page using code below:

```
ready('DOM_ELEMENT_SELECTOR', function (element) {
  let loginTextElement = document.createElement('p';
  loginTextElement.innerText = "CUSTOM_TEXT";
  parentNode.parentNode.insertBefore(loginTextElement, parentNode.nextSibling);
});
```
`DOM_ELEMENT_SELECTOR` can be any [CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp) from the Lock DOM that you wish to insert your custom text after.

`CUSTOM_TEXT` is the text that will be displayed.


Disclaimer: Auth0 Lock includes a lot of [UI customizations](https://auth0.com/docs/libraries/lock/v11/ui-customization) built-in already. Overriding the default look and feel via custom JS/CSS is not recommended unless there are no other options available. Later versions of Lock may lead to this code not working or requiring changes.
