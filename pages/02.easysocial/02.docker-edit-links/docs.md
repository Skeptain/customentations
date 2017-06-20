---
title: 'Docker Edit Links'
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

```js
<li>
		<a href="<?php echo ESR::profile();?>">
		<i class="fa fa-male"></i>
		<span><?php echo JText::_('COM_EASYSOCIAL_PROFILE');?></span>
	</a>
</li>
```

You can easily modify this by replacing the link and the icon. For having another link just replace this
```js
<?php echo ESR::profile();?>
```
by the URL you like. In example the default community profile page:
```js
/community/profile
```

The overview of all available FontAwesome icons you can find here: http://fontawesome.io/icons/ Just take the code from there and replace this:
```js
fa fa-male
```
by the icon code provided on the FontAwesome page.
