Instructions

- enable module
- go to "admin/structure/cm2-redirect"
- fill out settings and save
- un-comment line in settings.php where it says "$cookie_domain = '.example.com';" 
	Change value to your custom domain name. Leave the . in front of the domain. This allows the cookie to leave under both
	mobile and non-mobile domains
	
A new link will appear in the default Navigatio menu. The link is called  "Redirect". 
You can change the title of this link in the menu configuratio screen.

To change the text of the redirect link, use theme_cm2_link on your template.php file as follows:

/**
 * theme menu_link
 */
function MYTHEME_cm2_link($vars) {
  if (strstr($vars['path'],"redirect/mobile")) {
  	$vars['text'] = t('Mobile Version');
  }
  if (strstr($vars['path'],"redirect/desktop")) {
  	$vars['text'] = t('Full Version');
  }
  return theme_link($vars);
}
