---
title: HTL Global Objects
seo-title: HTL Global Objects
description: Without having to specify anything, HTL provides access to all objects that were commonly available in JSP after including global.jsp.
seo-description: Without having to specify anything, HTL provides access to all objects that were commonly available in JSP after including global.jsp. 
uuid: e03affbb-a683-4323-8224-53d8ef59caef
contentOwner: User
products: SG_EXPERIENCEMANAGER/HTL
topic-tags: html-template-language
content-type: reference
discoiquuid: fe071a7e-0dae-45c1-9f86-80c558483f87
mwpw-migration-script-version: 2017-10-12T21 46 58.665-0400
---

# HTL Global Objects{#htl-global-objects}

Without having to specify anything, HTL provides access to all objects that were commonly available in JSP after including `global.jsp`. These objects are in addition to any that may be introduced through the [Use-API](use-api.md).

## Enumerable Objects {#enumerable-objects}

These objects provide convenient access to commonly used information. Their content can be accessed with the dot notation, and they can be iterated-through using `data-sly-list` or `data-sly-repeat`.

|Variable Name|Description|
|--- |--- |
|properties|List of properties of the current Resource. Backed by [org.apache.sling.api.resource.ValueMap](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/reference-materials/javadoc/org/apache/sling/api/resource/ValueMap.html)|
|pageProperties|List of page properties of the current Page. Backed by [org.apache.sling.api.resource.ValueMap](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/reference-materials/javadoc/org/apache/sling/api/resource/ValueMap.hmtl)|
|inheritedPageProperties|List of inherited page properties of the current Page. Backed by [org.apache.sling.api.resource.ValueMap](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/reference-materials/javadoc/org/apache/sling/api/resource/ValueMap.html)|


## Java-backed Objects {#java-backed-objects}

Each of the following objects is backed by the corresponding Java object.

| Variable Name |Description |  |
|---|---|---|
| `component` | `com.day.cq.wcm.api.components.Component` |  |
| `componentContext` | `com.day.cq.wcm.api.components.ComponentContext` |  |
| `currentDesign` | `com.day.cq.wcm.api.designer.Design` |  |
| `currentNode` | `javax.jcr.Node` |  |
| `currentPage` | `com.day.cq.wcm.api.Page` |  |
| `currentSession` | `javax.servlet.http.HttpSession` |  |
| `currentStyle` | `com.day.cq.wcm.api.designer.Style` |  |
| `designer` | `com.day.cq.wcm.api.designer.Designer` |  |
| `editContext` | `com.day.cq.wcm.api.components.EditContext` |  |
| `log` | `org.slf4j.Logger` |  |
| `out` | `java.io.PrintWriter` |  |
| `pageManager` | `com.day.cq.wcm.api.PageManager` |  |
| `reader` | `java.io.BufferedReader` |  |
| `request` | `org.apache.sling.api.SlingHttpServletRequest` |  |
| `resolver` | `org.apache.sling.api.resource.ResourceResolver` |  |
| `resource` | `org.apache.sling.api.resource.Resource` |  |
| `resourceDesign` | `com.day.cq.wcm.api.designer.Design` |  |
| `resourcePage` | `com.day.cq.wcm.api.Page` |  |
| `response` | `org.apache.sling.api.SlingHttpServletResponse` |  |
| `sling` | `org.apache.sling.api.scripting.SlingScriptHelper` |  |
| `slyWcmHelper` | `com.adobe.cq.sightly.WCMScriptHelper` |  |
| `wcmmode` | `com.adobe.cq.sightly.SightlyWCMMode` |  |
| `xssAPI` | `com.adobe.granite.xss.XSSAPI` |  |

## JavaScript-backed Objects {#javascript-backed-objects}

There are also objects available that are backed by JavaScript. However, as of AEM 6.2 these objects are still experimental and it is better to use the Java-backed objects, which allow to do the same.

<!-- 

Comment Type: draft

<p> </p> 
<p>JS-specific context variables: These supply access to asynchronous implementions of all the Java objects listed below). To write HTL code that is protable to granite.js, you must use the variables provided by aem and sly, not the native Java variables.</p> 
<ul> 
 <li>wcm
  <ul> 
   <li>currentPage</li> 
   <li>nativePage: [com.day.cq.wcm.apiPage]</li> 
   <li>properties: {<i>enumerable</i>}</li> 
  </ul> </li> 
 <li>granite
  <ul> 
   <li>request
    <ul> 
     <li>parameters: {<i>enumerable</i>}</li> 
     <li>nativeRequest: [org.apache.sling.scripting.core.impl.helper.OnDemandReaderRequest]</li> 
     <li>pathInfo
      <ul> 
       <li>nativePathInfo: [SlingRequestPathInfo: path='/content/geometrixx/en/jcr:content/par/text', selectorString='null', extension='html', suffix='null']</li> 
      </ul> </li> 
    </ul> </li> 
   <li>resource
    <ul> 
     <li>nativeResource: [Paragraph, path=/content/geometrixx/en/jcr:content/par/text, type=wcm/foundation/components/text, cssClass=default, column=0/0, diffInfo=[null], resource=[JcrNodeResource, type=wcm/foundation/components/text, superType=null, path=/content/geometrixx/en/jcr:content/par/text]]</li> 
     <li>path: "/content/geometrixx/en/jcr:content/par/text"</li> 
     <li>properties: {sling:resourceType,jcr:created,jcr:lastModified,jcr:createdBy, textIsRich,jcr:lastModifiedBy,jcr:primaryType}</li> 
    </ul> </li> 
   <li>properties: {sling:resourceType,jcr:created,jcr:lastModified,jcr:createdBy, textIsRich,jcr:lastModifiedBy,jcr:primaryType}</li> 
  </ul> </li> 
</ul> 
<p>JS specific non-HTL related variables. Present due to JS-implementaion. Generally not used in templating:</p> 
<ul> 
 <li>console: JS Object</li> 
 <li>exports: JS Object</li> 
 <li>module: JS Object</li> 
 <li>setImmediate: JS Function</li> 
 <li>setTimeout: JS Function</li> 
 <li>use: JS Function</li> 
</ul>
-->
