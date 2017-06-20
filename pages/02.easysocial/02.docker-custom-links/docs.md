---
title: 'Docker Custom Links'
taxonomy:
    category:
        - docs
---

**Joomla**: 3.7.2</br>
**EasySocial**: 2.0.19</br>
**Docker**: 2.0.6</br>
**File**: /plugins/system/docker/themes/default.php</br>
**Override**: unknown

![](https://customizings.net/imgs/docker-ownlinks.png)

Open **default.php** and you will find this code. This is one of many links inside the docker plugin menu. Each link looks like this:

```php
<li>
		<a href="<?php echo ESR::profile();?>">
		<i class="fa fa-male"></i>
		<span><?php echo JText::_('COM_EASYSOCIAL_PROFILE');?></span>
	</a>
</li>
```

To replace the existing link with your custom link, replace this it by your desired URL:
```js
<?php echo ESR::profile();?>
```

The overview of all available FontAwesome icons you can find here: http://fontawesome.io/icons/ Just take the code from there and replace this:
```js
fa fa-male
```

To change the link title go for this and replace it by your own title. You can also search your language file for this string and replace the translation there:
```js
COM_EASYSOCIAL_PROFILE
```

