---
title: 'Stop Moving Page by Loading'
taxonomy:
    category:
        - docs
---

**Joomla**: 3.7.2</br>
**EasySocial**: 2.0.19</br>
**Docker**: 2.0.6</br>

If you got your Docker position on top you will recognize that your site moves down while loading your page. I think this is not good so I found to solution that stops this. You should know where your custom.css of your template is, because we need to add some CSS to it.

At first you should make sure that your Docker is positioned on **bottom**. Yes, sounds strange but it is no typo. Now add the following to your custom.css:

```css
#es.es-docker.is-bottom {
	height: 44px;
	top: 0; }

#es.es-docker.is-bottom.active-menu .docker-popup-window, #es.es-docker.is-bottom.active-mobile-login .docker-popup-window {
	margin-top: 50px !important;
	top: 0 !important;
	margin-bottom: inherit !important;
	bottom: inherit !important; }

#es.es-docker.is-bottom.active-quickpost .docker-popup-quickpost {
	margin-top: 50px !important;
	top: 0 !important;
	margin-bottom: inherit !important;
	bottom: inherit !important; }
```

You will now see that your site is no longer pushed downwards when the docker is loaded.