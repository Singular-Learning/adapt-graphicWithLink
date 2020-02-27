# adapt-graphicWithLink  

**Graphic With Link** is a *presentation component* based on [adapt-contrib-graphic](https://github.com/adaptlearning/adapt-contrib-graphic), bundled with the [Adapt framework](https://github.com/adaptlearning/adapt_framework).  

**Graphic With Link** displays graphic content that has been optimized for various devices. The component swaps out images based upon the device's screen size. The image is linked to an external URL

## Installation

Like all external compontents it has to be installed in the Adapt framework and in the Adapt authoring tool in order to be used.

With the [Adapt CLI](https://github.com/adaptlearning/adapt-cli) installed, run the following from the command line:  
`adapt install adapt-graphicWithLink `

    Alternatively, this component can also be installed by adding the following line of code to the *adapt.json* file:  
    `"adapt-graphicWithLink ": "*"`  
    Then running the command:  
    `adapt install`  
    (This second method will reinstall all plug-ins listed in *adapt.json*.)

In order to use **Graphic With Link** in the Adapt authoring tool, you have to install it using the [Plug-in Manager](https://github.com/adaptlearning/adapt_authoring/wiki/Plugin-Management).

* If **Graphic With Link** has been uninstalled from the Adapt framework or Adapt authoring tool, it may be reinstalled as above.

## Settings Overview

The attributes listed below are used in *components.json* to configure **Graphic With Link**, and are properly formatted as JSON in [*example.json*](https://gitlab.com/singular-adapt/adapt-graphicWithLink/blob/master/example.json).

### Attributes

[**core model attributes**](https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes): These are inherited by every Adapt component.

**\_component** (string): This value must be: `graphicwithlink`.

**\_classes** (string): CSS class name to be applied to **Graphic With Link**’s containing `div`. The class must be predefined in one of the Less files. Separate multiple classes with a space.

**\_layout** (string): This defines the horizontal position of the component in the block. Acceptable values are `full`, `left` or `right`.  

**instruction** (string): This optional text appears above the component. It is frequently used to
guide the learner’s interaction with the component.  

**\_graphic** (object): The image that constitutes the component. It contains values for **alt**, **large**, and **small**.

>**alt** (string): This text becomes the image’s `alt` attribute. 

>**large** (string): File name (including path) of the image used with large device width. Path should be relative to the *src* folder (e.g., *course/en/images/origami-menu-two.jpg*).  

>**small** (string): File name (including path) of the image used with small device width. Path should be relative to the *src* folder (e.g., *course/en/images/origami-menu-two.jpg*).  

>**attribution** (string): Optional text to be displayed as an [attribution](https://wiki.creativecommons.org/Best_practices_for_attribution). By default it is displayed below the image. Adjust positioning by modifying CSS. Text can contain HTML tags, e.g., `Copyright © 2020 by <b>John Doe</b>`

>**url** (string): The url that will be openened when you click on the image. The url will be opened in a new window.

## Accessibility
+ Remember to include an **alt** attribute for all your images. Screen readers will read aloud alt text content, so leave the alt text empty (`"alt": ""`) if the image does not contribute significant course content.  
+ If the alt text is left empty, the image will *not* be included in the tab order. If the component is configured to display [title or body text]((https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes)), these will remain keyboard accessible.  
+ If the alt text is assigned a value, but the component is not being tracked for course completion, assign the class `"no-state"` to **\_classes**. Adapt's accessibility mode reports to the learner the 'state' of the component, whether it is complete or incomplete. It is not common practice to require interaction with (or 'completion' of) an image for course completion. Indeed, a screen reader needlessly announcing the state of an image may be distracting for the learner. Assigning the built-in class `"no-state"` prevents this.  

## Limitations

No known limitations.

----------------------------
**Version number:**  1.0.0  <a href="https://singularlearning.com/" target="_blank"><img src="https://singularlearning.com/logo/singularLearning.png" alt="singularLearning logo" align="right"></a>  
**Version number Plugin Based:** 4.0.0  
**Framework versions:** 5+  
**Author / maintainer:** Singularlearning Team
**Accessibility support:** WAI AA  
**RTL support:** Yes  
**Cross-platform coverage:** Chrome, Chrome for Android, Firefox (ESR + latest version), Edge, IE11, Safari 12+13 for macOS/iOS/iPadOS, Opera  
