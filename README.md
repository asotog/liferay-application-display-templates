# Liferay Application Display Templates #

<strong>Note:</strong> application display templates is a new feature introduced in LR 6.2

## images-infinite-grid-view.vm ##

Velocity template ( [images-infinite-grid-view.vm](https://github.com/asotog/liferay-application-display-templates/blob/master/images-infinite-grid-view.vm) ) implemented for asset publisher, webcontent asset entries will be displayed as thumbnailed items, and provides ajax lazy loading mechanism following the infinite scrolling approach on its UX/UI, it requests the items using [Liferay javascript JSON api](https://github.com/asotog/liferay-application-display-templates/blob/master/images-infinite-grid-view.vm#L67) for service calls to retrieve the entries data on each scroll when are needed more items.

Additionally the articles that are going to be displayed within this template will require to use the following journal article structure [content-images-structure.xml](https://github.com/asotog/liferay-application-display-templates/blob/master/webcontent-structures/content-images-structure.xml) and article template [content-images-templates.vm](https://github.com/asotog/liferay-application-display-templates/blob/master/webcontent-templates/content-images-templates.vm) in order to provide the thumbnail image and the description

##### Asset Publisher configuration #####

Once selected this display template from asset publisher, this template will receive the following configuration settings to start working:

- <strong>delta</strong> (number of items to be displayed per page or per scrolling in this template)
- <strong>scopes</strong> (scopes from the sites where are going to be retrieved the entries, by default is current site where asset publisher is placed)
- <strong>journal article template</strong> (which article template is going to be used to filter the entries that are going to be displayed, should be selected a template created with the article structure specified above)

![Alt text](http://asotog.github.io/liferay-application-display-templates/screenshots/screenshot1.png)
