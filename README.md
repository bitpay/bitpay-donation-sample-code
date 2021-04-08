# Donation Template

## Overview

This template is designed to allow a user to copy and paste into an existing website with minimal config to accept BitPay Donations.

# Requirements

This plugin requires the following:

* A BitPay merchant account ([Test](http://test.bitpay.com) and [Production](http://www.bitpay.com))

# Installation

To install, copy and paste into an existing page (including css references, jquery, etc).  You may need to adjust file paths.

# Configuration

* Change the header/footer placeholder text as needed
* If there is a **maximum donation amount**, update the Javascript in the `submitForm` function.
* To add more/less pre-defined rows, copy and paste the existing row/columns, and update the values as needed.
	* you will also need to add/remove these values in the `$payment_arr` array, located in the `updateCSS` function.
* Login to your BitPay dashboard ([Test](http://test.bitpay.com/dashboard) or [Production](http://www.bitpay.com/dashboard))
* Click **Payment Tools** on the left
* Click **Donation Buttons**
	* If you do not see this, you will need to contact our compliance team at [compliance@bitpay.com](mailto:compliance@bitpay.com)
* Click **Generate**
	*Scroll down and look for the following ```<input type="hidden" name="data" value = "<long string of characters">```

* Scroll down to the bottom of the html and look for ```$env = "test"```
	* If you are in `test` mode, do not change this value, as it is the default
* Copy the value from the `Donation Button` source code to either the `$test_token` and/or `$prod_token`
* Edit the **redirectURL** value to redirect users after a payment is made

**Configuration** is now complete.

## License

[GNU General Public License version 3 (GPLv3)](https://github.com/opencart/opencart/blob/master/license.txt)

