FROM 3scale/openresty

## add your supervisor openresty config
ADD openresty.conf /etc/supervisor/conf.d/

# Add your app
ADD ./app /var/www

EXPOSE 80

CMD ["supervisord", "-n"]
