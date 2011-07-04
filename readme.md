#TemplatesToJs

TemplatesToJs is a ruby class which will take a directory of templates and format them as string values in a javascript object. The advantage of this is the ability to use the same directory of templates for both back end and front end rendering.

##Usage:

    template_joiner = TemplatesToJs.new({
      :template_dir    => 'templates', #Defaults to "templates"
      :template_format => 'mustache',  #Defaults to "mustache"
      :js_object_name  => 'templates',  #Defaults to "templates"
      :output          => 'output/mytemplates.js'  #Path to write .js file, Defaults to false
    })
    template_joiner.write_js
    puts template_joiner.js
    
##Outputs:

    templates = {
        'template_1' : '<div id="template_1"><h1 id="title">{{title}}</h1></div>',
        'template_2' : '<div id="another_template"><h2 id="title">{{title}}</h2></div>'
    };