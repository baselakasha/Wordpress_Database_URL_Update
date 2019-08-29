# Wordpress Database URL Update

Use this code to update the urls in you database when you upload your website from localhost to hosting or when you change your website domain name.


```
UPDATE wp_options SET option_value = replace(option_value, 'OLD_URL', 'NEW_URL') WHERE option_name = 'home' OR option_name = 'siteurl'; 
UPDATE wp_posts SET post_content = replace(post_content, 'OLD_URL', 'NEW_URL');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'OLD_URL','NEW_URL');
UPDATE wp_usermeta SET meta_value = replace(meta_value, 'OLD_URL','NEW_URL'); 
UPDATE wp_links SET link_url = replace(link_url, 'OLD_URL','NEW_URL');
UPDATE wp_comments SET comment_content = replace(comment_content , 'OLD_URL','NEW_URL');
UPDATE wp_posts SET guid = replace(guid, 'OLD_URL','NEW_URL')
```

Replace OLD_URL by your website old URL and replace NEW_URL by your new website URL

Execute the code in your database using PHPMyAdmin or MySQL command line.

[Code in .txt file](https://github.com/baselakasha/Wordpress_Database_URL_Update/blob/master/Wordpress_Database_URL_Update.txt)
