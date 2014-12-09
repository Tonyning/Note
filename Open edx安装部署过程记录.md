## Open edx安装部署过程记录

1. Open edx配置SMTP</br>
在`/edx/app/edxapp/edx-platform/cms/envs/common.py`中添加一下配置：
`EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'` 
`EMAIL_HOST = 'smtp.example.org'`</br>
`EMAIL_PORT = 25`</br>
`EMAIL_USE_TLS = True`</br>
`EMAIL_HOST_USER = 'admin@example.com'`</br>
`EMAIL_HOST_PASSWORD = 'passwd'`</br>
`DEFAULT_FROM_EMAIL = 'from@example.com'` 
`DEFAULT_FEEDBACK_EMAIL = 'feedback@example.com'` 
`SERVER_EMAIL = 'devops@example.com' ADMINS = () MANAGERS = ADMINS`


