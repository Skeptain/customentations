---
title: 'EasySocial Header on Favorites'
taxonomy:
    category:
        - docs
---

**Joomla**: 3.7.2</br>
**EasySocial**: 2.0.19</br>
**JReviews**: 2.7.17.2</br>
**File**: /com_jreviews/jreviews/views/themes/default/listings/listings_favorites.thtml</br>
**Override**: /templates/jreviews_overrides/views/themes/spielerschaft/listings/listings_favorites.thtml</br>

Open **listings_favorites.thtml** inside your override folder and search for the following code:

```php
<?php /* PAGE HEADER */ ?>
```

Below that row insert the following code:

```php
<?php
$uri = JFactory::getURI();
$absolute_url = $uri->toString();
$testid = JString::str_ireplace( 'FULL LINK WITHOUT ID' , '' , $absolute_url );        
require_once(JPATH_ADMINISTRATOR . '/components/com_easysocial/includes/easysocial.php'); 
$esuser = ES::user($testid); ?> 
<div id="es" class="es"> <?php echo ES::template()->html('html.miniheader', $esuser); ?> </div>
?>
```

FULL LINK WITHOUT ID means you pick the URL from the browser when you are on the favorites list page of any user. It should look similar to this: https://domain/jreviews/favorites?user= followed by the id. You need to remove the id from the URL before pasting the code into your file!