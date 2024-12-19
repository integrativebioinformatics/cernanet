# cernanet
A comprehensive database for microRNA-mRNA and microRNA-lncRNA interactions

## Acceso a la Red

La red de interacciones está disponible en el siguiente enlace: https://drive.google.com/drive/folders/1-5BDGsogh7k9JxXNrRKkY-rXRpTd4vcU?usp=drive_link

# README

## Descripción del Archivo

El archivo `catalogo_interacciones_cerna_status.txt` contiene un catálogo de interacciones entre miRNAs, mRNAs y lncRNAs en el genoma humano. Este catálogo forma parte de una red de ceRNAs (competing endogenous RNAs) y se generó utilizando datos de diversas bases de datos y herramientas bioinformáticas.

## Formato del Archivo

El archivo está estructurado en columnas con los siguientes encabezados:

- `mRNA`: Identificador del mRNA (ENSG).
- `miRNA`: Identificador del miRNA (hsa-miR).
- `Status_coding`: Estado de validación del mRNA (validado o predicho).
- `lncrna`: Identificador del lncRNA (ENSG).
- `status_lncrna`: Estado de validación del lncRNA (validado o predicho).

### Ejemplo de Contenido

```
mRNA    miRNA   Status_coding   lncrna  status_lncrna
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000080947 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000126005 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000131797 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000163597 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000175061 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000177725 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000177736 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000178722 validated
ENSG00000000003 hsa-miR-124-3p  validated       ENSG00000180867 validated
```

## Metodología

### 1. Generación del Catálogo de Interacciones entre miRNAs y mRNAs

- **Referencia de miRNAs**: Se utilizaron los miRNAs humanos disponibles en la base de datos miRBase v22.1 (Kozomara et al., 2019).
- **Referencia de mRNAs**: Se utilizaron los transcritos y anotaciones disponibles en GENCODE versión M29 (Frankish et al., 2019).
- **Fuentes de Interacciones**: Las interacciones entre miRNAs y mRNAs se recopilaron de las bases de datos TargetMiner, miRDB, TargetScanHuman y TarBase v8.0.
- **Categorización**: Las interacciones se clasificaron como validadas experimentalmente o predichas computacionalmente. Solo se consideraron las interacciones predichas presentes en al menos tres de las bases de datos utilizadas.

### 2. Generación del Catálogo de Interacciones entre miRNAs y lncRNAs

- **Fuentes de Interacciones**: Se utilizaron las bases de datos LncBase y starBase para recuperar las interacciones entre miRNAs y lncRNAs.
- **Categorización**: Las interacciones validadas experimentalmente se consideraron reales, mientras que las predichas se mantuvieron como tales.

### 3. Unificación de la Red Global

- **Integración**: La red final de interacciones se recopiló utilizando scripts desarrollados en Perl, Python y R.
- **Visualización**: La red se visualizó utilizando Cytoscape (Shannon et al., 2003).

## Referencias

- Kozomara, A., Birgaoanu, M., & Griffiths-Jones, S. (2019). miRBase: from microRNA sequences to function. Nucleic Acids Research, 47(D1), D155-D162.
- Frankish, A., et al. (2019). GENCODE reference annotation for the human and mouse genomes. Nucleic Acids Research, 47(D1), D766-D773.
- Bandyopadhyay, S., & Mitra, R. (2009). TargetMiner: microRNA target prediction with systematic identification of tissue-specific negative examples. Bioinformatics, 25(20), 2625-2631.
- Wong, N., & Wang, X. (2015). miRDB: an online resource for microRNA target prediction and functional annotations. Nucleic Acids Research, 43(W1), W135-W141.
- Agarwal, V., et al. (2015). Predicting effective microRNA target sites in mammalian mRNAs. eLife, 4, e05005.
- Karagkouni, D., et al. (2018). DIANA-TarBase v8: a decade-long collection of experimentally supported miRNA-gene interactions. Nucleic Acids Research, 46(D1), D239-D245.
- Paraskevopoulou, M. D., et al. (2015). DIANA-LncBase v2: indexing microRNA targets on non-coding transcripts. Nucleic Acids Research, 44(D1), D231-D238.
- Li, J. H., et al. (2013). starBase v2.0: decoding miRNA-ceRNA, miRNA-ncRNA and protein-RNA interaction networks from large-scale CLIP-Seq data. Nucleic Acids Research, 42(D1), D92-D97.
- Shannon, P., et al. (2003). Cytoscape: a software environment for integrated models of biomolecular interaction networks. Genome Research, 13(11), 2498-2504.
