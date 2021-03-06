## pytcga

Python library for accessing and processing public TCGA data


## Examples

#### Loading Clinical Data
```python

import pytcga

# Downloading and loading LUAD patient data
clinical = pytcga.load_clinical_data('luad')
```

#### Loading Mutation Data

```python
import pytcga

# Downloading and loading LUAD mutations
luad_mutations = \
    pytcga.load_mutation_data(disease_code='LUAD', with_clinical=False)


# Also appends clinical data with `with_clinical` flag
luad_mutations = \
    pytcga.load_mutation_data(disease_code='LUAD', with_clinical=True)

# Filter variants with the `variant_type` argument
# variant_type = {'all', 'indel', SNP', 'INS', 'DEL'}
luad_indel_mutations = \
    pytcga.load_mutation_data(disease_code='LUAD', with_clinical=True, variant_type='indel')

```

#### Loading RNASeq Data
```python
import pytcga

# Downloading and loading LUAD gene quantification
luad_rnaseq = \
    pytcga.load_rnaseq_data(disease_code='LUAD', with_clinical=True)

```

