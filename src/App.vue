
<template>
<div>
<ejs-richtexteditor id="mentionIntegration" >
 </ejs-richtexteditor>
                        
<ejs-mention target='#mentionIntegration' :dataSource='commentsData' :fields='commentsfields'
 popupHeight="200px" popupWidth="250px" showMentionChar="true" mentionChar='#' suffixText=" Welcome!"
 allowSpaces="true" sortOrder="Ascending" filterType="EndsWith" ></ejs-mention>
</div>
</template>
<script>
import { MentionComponent } from "@syncfusion/ej2-vue-dropdowns";
import { RichTextEditorComponent,Toolbar,Link,Image,HtmlEditor } from "@syncfusion/ej2-vue-richtexteditor";
export default {
        components: {
            'ejs-mention': MentionComponent,
            'ejs-richtexteditor':RichTextEditorComponent
        },
         provide: {
        richtexteditor: [Toolbar, Link, Image, HtmlEditor]
  },
        data: function() {
        return {
          commentsfields : { text: 'Name' },
          commentsData : [ { Name: "Selma Rose", EmailId: "selma@gmail.com"},
            { Name : "Maria", EmailId : "maria@gmail.com" },
            { Name : "Russo kay", EmailId : "russo@gmail.com" },
            { Name : "Robert", EmailId : "robert@gmail.com" },
            { Name : "Garth", EmailId : "garth@gmail.com" }]
        };
    }
}
</script>


<style>
</style>