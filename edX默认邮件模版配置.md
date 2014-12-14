```    
<%namespace file="../main.html" import="stanford_theme_enabled" />
<%! from django.utils.translation import ugettext as _ %>
${_("Thank you for signing up for {platform_name}.").format(platform_name=settings.PLATFORM_NAME)}

${_("To get started, please activate your account by clicking on the link below"
      " (you may also copy and paste the link into your browser's address"
      " bar).").format(platform_name=settings.PLATFORM_NAME)}

% if is_secure:
  https://${ site }/activate/${ key }
% else:
  http://${ site }/activate/${ key }
% endif

% if settings.PLATFORM_NAME == "edX":
${_("Activation ensures that you can register for {platform_name} courses and"
      " access the courseware."
      " If you require assistance, please use our web form at"
      " {contact_us} or email {info_address}.").format(
             platform_name=settings.PLATFORM_NAME,
             contact_us='https://www.edx.org/contact-us',
             info_address=settings.CONTACT_EMAIL
      )}    
      ```
