# dita-relaxng-defaults
DITA Open Toolkit 2.x plugin which allows the DITA OT parser to process default attribute values specified in RelaxNG schemas.
DITA OT 2.x already comes with the Relax NG schemas for the DITA 1.3 vocabulary so you just need to install this plugin (copy the folder "dita-relaxng-defaults" to the plugins folder and run the integrator) in your DITA OT 2.x and you will be able to publish RNG-based DITA Maps and Topics using the command line "dita.bat" or "dita.sh".

In order for the plugin to properly find RNG or RNC schemas associated to the XML documents, they need to be referenced at the beginning of the XML documents using the xml-model processing instruction like:

         <?xml-model href="urn:oasis:names:tc:dita:rng:topic.rng" schematypens="http://relaxng.org/ns/structure/1.0"?>
         
If you are referring to a custom RNG-based DITA specialization, the specialization DITA OT plugin needs to map using <system> mappings in the plugin's catalog.xml the reference to a RelaxNG file like:
  
          <system systemId="urn:oasis:names:tc:dita:rng:topic.rng" uri="rng/topic.rng"/>

The JAR libraries for this plugin have been either copied from or generated using the GitHub project:
https://github.com/georgebina/dita-ng
