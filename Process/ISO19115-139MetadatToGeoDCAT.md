# ISO-19115-3 to GeoDCAT-AP Conversion Guide

## Objective

Convert ISO‑19115‑3 metadata XML file into GeoDCAT‑AP RDF, so metadata of a dataset can be integrated directly into the RDF file of the ontology instead of manual editing in Protégé.

## Step-by-Step Instructions

### Step 1: Download the Source Metadata File
1. Navigate to your dataset source. *(Example: [BD-Haie Dataset on carte.gouv.fr](https://cartes.gouv.fr/rechercher-une-donnee/dataset/IGNF_BD-HAIE)).*
2. Download the metadata file in ISO-19115-3 XML format.

### Step 2: Convert ISO-19115-3 to ISO-19139
Because the SEMIC transformation tool requires the older ISO-19139 standard, you must first downgrade the XML schema.

1. If your downloaded file contains wrapper tags like `<csw:GetRecordByIdResponse>` or `<csw:Record>`, manually remove them.

2. Choose one of the following GeoNetwork methods to perform the conversion:
   * Option A (Local): Use GeoNetwork Desktop. See the [GeoNetwork Documentation](https://docs.geonetwork-opensource.org/4.2/fr/).
   * Option B (Web): Use the [GeoNetwork Online Converter](https://geonetwork.github.io/geonetwork-ui/simple-editor/).

### Step 3: Transform ISO-19139 XML into GeoDCAT-AP RDF
Use the official European Commission (SEMIC EU) XSLT transformation components.

1. Clone the official SEMIC repository:
    ```sh
    git clone https://github.com/SEMICeu/iso-19139-to-dcat-ap
    ```

2. Follow the instructions in the documentation to use the python script and generate the GeoDCAT-AP rdf file: [HowTo guide](https://github.com/SEMICeu/iso-19139-to-dcat-ap/blob/main/documentation/HowTo.md)

