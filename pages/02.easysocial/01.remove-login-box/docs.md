---
title: 'Remove Login Box'
taxonomy:
    category:
        - docs
---

**Joomla**: 3.7.2</br>
**EasySocial**: 2.0.19</br>
**File**: /components/com_easysocial/themes/wireframe/dashboard/guests/default.php</br>
**Override**: /templates/template/html/com_easysocial/dashboard/guests/default.php</br>

![](https://customizings.net/imgs/login-box.png)

Open **default.php** file inside your override folder and remove the following code:

```js
<div>
	<?php echo $this->html('html.login', $return); ?>
</div>
```

It is important to remove it inside the file instead of hiding it per CSS. If you hide it by CSS the reCaptcha will still remain inside the box though it is hidden. Due to that you will not be able to have a quick register module with another reCaptcha there. If you remove the line inside the file, the reCaptcha will work fine inside your quick register module.
