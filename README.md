# FormBuilderBlueFire - BlueFire Payment Integration for ProcessWire FormBuilder
Developed by Mike Spooner (thetuningspoon) for Solution Innovators

Uses BlueFire's Checkout API to process payments following a FormBuilder form submission, redirecting to BlueFire's site for payment. Delays sending of admin/autoresponder emails until payment is completed.

##Usage

1. Install module and enter BlueFire account information in the module's settings. 

2. In the template for your confirmation page, call $modules->FormBuilderBlueFire->processCompletedPayment() to trigger the emails to be sent and the completion flag to be set in the entries database. This method will return the updated form entry (array) if successful, or false if not.

BlueFire does not have a test mode for the Checkout API, but you can contact them to request they put your account in demo mode.