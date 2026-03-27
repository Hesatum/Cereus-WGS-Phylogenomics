Este repositório contém o workflow completo de bioinformática utilizado na minha dissertação de Mestrado. O objetivo é reconstruir a história evolutiva do complexo de espécies Cereus utilizando dados de sequenciamento de genoma completo (WGS) e uma abordagem de coalescência multiespécies.

🧬 Estrutura do Projeto
A arquitetura de pastas segue o fluxo sequencial do processamento, garantindo que cada etapa gere inputs rastreáveis para a fase seguinte:

.
├── 00_rawdata/           # Dados brutos (FastQ)
├── 01_trimmed_data/      # Reads filtradas e adaptadores removidos
├── 02_alignment_bam/     # Mapeamento contra o genoma de referência
├── 03_variant_calling/   # VCFs individuais (GVCF)
├── 04_joint_genotyping/  # Genotipagem conjunta (VCF populacional)
├── 05_loci_extraction/   # Extração de sequências via Virtual Spliceosome
├── 06_alignments/        # Alinhamentos múltiplos (MSA) por locus
├── 07_trimmed_fasta/     # Alinhamentos polidos
├── 08_gene_trees/        # Árvores de genes individuais
└── scripts/              # Scripts customizados e utilitários
