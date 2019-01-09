# Abstract class hierachy
- Plugin (pkp-lib/classes/plugins/Plugin.inc.php)
-- AuthPlugin (pkp-lib/classes/plugins/AuthPlugin.inc.php)
-- LazyLoadPlugin (pkp-lib/classes/plugins/LazyLoadPlugin.inc.php)
--- BlockPlugin (pkp-lib/classes/plugins/BlockPlugin.inc.php)
--- GatewayPlugin (pkp-lib/classes/plugins/GatewayPlugin.inc.php, cf ojs/plugins/gateways/resolver/README)
--- GenericPlugin (pkp-lib/classes/plugins/GenericPlugin.inc.php)
---- PKPViewableFilePlugin (pkp-lib/classes/plugins/PKPViewableFilePlugin.inc.php)
--- ImportExportPlugin (pkp-lib/classes/plugins/ImportExportPlugin.inc.php)
--- PKPPubIdPlugin (pkp-lib/classes/plugins/PKPPubIdPlugin.inc.php)
--- PaymethodPlugin (pkp-lib/classes/plugins/PaymethodPlugin.inc.php)
--- LazyLoadPlugin (pkp-lib/classes/plugins/LazyLoadPlugin.inc.php)
-- MetadataPlugin (pkp-lib/classes/plugins/MetadataPlugin.inc.php)
-- OAIMetadataFormatPlugin (pkp-lib/classes/plugins/OAIMetadataFormatPlugin.inc.php)
-- ReportPlugin (pkp-lib/classes/plugins/ReportPlugin.inc.php)



# Layout of a plugin
- /plugin
-- ./arbitrary_package_source
-- ./locale
--- ./Iso639_Iso3166@script (eg sr_RS@latin or en_US)
---- locale.xml
-- ./templates
-- ./tests
-- TitleCasePlugInNamePlugin.inc.php
-- index.php (requires the relevant source and returns a Plugin object)
-- settings.xml
-- version.xml

# index.php

# settings.xml
Settings name, type and default values
- plugin_settings
-- setting [@type]
--- name: String
--- value: serialize value approriate to setting/@type

# version.xml
Configuraton data describing this version of the plugin
- version
-- application:
-- type: category string?
-- release: release number, dot-separated
-- date: W3c date
-- lazy-load: [0,1]
