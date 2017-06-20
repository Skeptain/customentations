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

Open **default.php** and you will find the following code:

```js
<li>
		<a href="<?php echo ESR::profile();?>">
		<i class="fa fa-male"></i>
		<span><?php echo JText::_('COM_EASYSOCIAL_PROFILE');?></span>
	</a>
</li>
```

You can easily modify this part by replacing the link and the icon. Just replace this

´´´js
<?php echo ESR::profile();?>
```

by

```js
/URL/SUB-URL/...
```