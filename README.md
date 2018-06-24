# Internal Tools Included
This repo is a go to place for my fav code snippets that i found useful 
1. Custom Jenkins Dockerfile with EST Timezone and Java Env Settings that Enables HTML Serenity Report with Screenshoot
2. To get the List of installed plugins run this command ``` curl -sSL "http://bold:admin@35.207.6.62:9090/pluginManager/api/xml?depth=1&xpath=/*/*/shortName|/*/*/version&wrapper=plugins" | perl -pe 's/.*?<shortName>([\w-]+).*?<version>([^<]+)()(<\/\w+>)+/\1 \2\n/g'|sed 's/ /:/' ```
