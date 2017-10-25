MailChimp Service

<h3>MailChimp Service for Drupal 8 </h3>

The Drupal 8 module for MailChimp Service.

<h3>Installation</h3>

To install from this repository:

Clone the repository into your Drupal site modules directory:

<code>git clone https://github.com/rabithk/mailchimp_service.git /modules/mailchimp_service </code>

This module require <code>drewm/mailchimp-api": "^2.2</code>

Install mailchimp-api by adding <code>drewm/mailchimp-api": "^2.2"</code> in composer.json and <code>composer install</code>

Install the module, as usual, using Drush or the Drupal UI.

<h3>Configuration</h3>

Get Mailchimp API Key from http://admin.mailchimp.com/account/api
Configure Mailchimp API Key in admin/config/mailchimp_service/mailchimpserviceadmin


<h3> How to use API:</h3>

Example : 

<code>
    // Include service file in your file.
    use Drupal\mailchimp_service\MailchimpService;
    
    // Create profile array for mailChimp.
    $userProfile = [
      'FNAME' => 'FirstName of the user',
      'LNAME' => 'FirstName of the user,
    ];
    
    // Set type of sybscrption.
    $type = 'subscribed'; // Type can be 'Status','pending','Update','unsubscribed', or 'subscribed'
    
    // Subscription Email.
    $email = 'youremail@example.com';
    
    // MailChimp list id.
    $mail_chimp_list_id ='xxxx'; // Add MailChimp list id.
    
    $result = $this->mailchimpService->mailchimpSubscription($userProfile, $type, $email, $mail_chimp_list_id);
</code>

