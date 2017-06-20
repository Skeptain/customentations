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

Open your default.php file and remove the following code:

´´´js
<div>
	<?php echo $this->html('html.login', $return); ?>
</div>

