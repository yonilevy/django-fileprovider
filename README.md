# INSTALLATION  

  use pip to install package:  
  `pip install -e git+https://bitbucket.org/renlinx007/django-fileprovider.git@0.1a#egg=django-fileprovider`  

* add `fileprovider` to django `INSTALLED_APPS` section.  
* add `fileprovider.middleware.FileProviderMiddleware` to `MIDDLEWARE_CLASSES` section
* set django `settings` file with `FILEPROVIDER_NAME` any of  available providers {'python', 'nginx', 'apache'}

# USAGE  

 on django views where file response is required, fill response header `X-File` with absolute file path  
 for example,  

 ```python  
      
    def hello(request):
        response = HttpResponse()
        response['X-File'] = '/absolute/path/to/file'
        return response
 ```
