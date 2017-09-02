# QTI Content Player #

## Project Brief ##
* Convert a large amount of printed content to digital e-learning solution.
* Not to be server side - to be used in an unknown LMS Platform
* Data to be in the QTI XML format - a standard for e-learning assessment data
* Content to be Interactive and engaging but quick to produce

## Team ##
Built by [Jay Campbell](http://pyramidium.co.uk/), [Conorde Clarke](https://linkedin.com/in/conorde/), [Isaac Goldfarb](https://linkedin.com/in/isaac-goldfarb-0049851/), Klas Ericsson, [John Kavanagh](http://johnkavanagh.co.uk/), [Malcolm Mullafiroze](https://linkedin.com/in/ardalon/), [Nicky Rojas](http://www.nickyrojas.co.uk/), [Ewan Tavener](http://www.ewantavener.co.uk/)

Directed by [Samu Lang](https://linkedin.com/in/langsamu/)

Produced by [Mark Perry](https://linkedin.com/in/marksperry/)

## QTI Specification ##
A standard in e-learning. Utilising a standard that already exists, well documented and has been accepted in the industry.
https://www.imsglobal.org/question/qtiv2p2/QTIv2p2-ASI-InformationModelv1p0/imsqtiv2p2_asi_v1p0_InfoModelv1p0.html

## Research ##
Before we started actual production we need to find the correct technical solution. We explored the following technologies:
* OO Javascript - a custom framework converting XML to HTML manually.
* AngularJS - attaching directives to xml nodes (https://github.com/etavener/qti-player-angular/)
* XSLT - manipulating XML
* Polymer - Using the shadowDOM to render the XML as HTML web components.


## Challenges ##
During the research phase we faced the following challenges:
* AngularJS directives could only translude in one direction.
* AngularJS with OO Javascript is not elegant.
* XSLT is an old and complicated way of converting XML
* QTI XML although very well documented is a beast and very strict.
* QTI XML contains more than the presentation. It contains not visual data including variables, event handling and response processing.
* Polymer web components are very new
* A custom OO Javascript method was not transparent or easy for other developers

## Solution ##
We decided that Polymer was an ideal solution because:
* We could use it with XSLT (to create the polymer node names)
* Its a standard - web components
* We could utilise the shadowDOM and keep the original XML
* We could develop OO Javascript components that inherit other components. This means we could have an component inheritance similar to that in the QTI specification.

## Examples ##
Templates (T001 to T117) - Just change the link and refresh.

XML Data:
http://www.ewantavener.co.uk/demo/qti-player/templates/T001.xml
Rendered example:
http://www.ewantavener.co.uk/demo/qti-player/app/index.html?id=T001

XML Data:
http://www.ewantavener.co.uk/demo/qti-player/templates/T117.xml
Rendered example:
http://www.ewantavener.co.uk/demo/qti-player/app/index.html?id=T117
