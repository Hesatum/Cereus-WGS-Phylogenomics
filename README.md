O Mapa do Projeto (Estrutura de Diretórios)
A primeira regra de ouro da filogenômica é a organização espacial. Trabalharemos com arquivos que pesam dezenas de gigabytes e geraremos centenas de milhares de arquivos intermediários.

Para mantermos a sanidade e a reprodutibilidade, todo o nosso fluxo de trabalho obedecerá a esta estrutura cronológica de pastas. Recomendamos que você crie esta arquitetura no seu servidor ou HD antes de rodar o primeiro script:

Plaintext
Cereus-WGS-Project/
├── scripts/                 # Onde todos os nossos códigos (.sh, .py) vão morar
├── reference_genome/        # O genoma de referência (FASTA) e a anotação (GFF3)
├── 00_rawdata/              # Arquivos brutos vindos do sequenciador (.fastq.gz)
├── 01_trimmed_data/         # Reads limpos após o controle de qualidade (fastp)
├── 02_alignment_bam/        # Alinhamentos mapeados contra a referência (BWA)
├── 03_variant_calling/      # Arquivos GVCF individuais de cada cacto (GATK)
├── 04_joint_genotyping/     # O arquivo BCF final unificando todas as mutações
├── 05_loci_extraction/      # Os genes pescados pelo nosso Virtual Spliceosome
├── 06_alignments/           # Alinhamentos múltiplos brutos de cada gene (MAFFT)
├── 07_trimmed_fasta/        # Alinhamentos polidos livres de ruído (TrimAl)
└── 08_gene_trees/           # Árvores de genes individuais inferidas (IQ-TREE)
(Dica: A numeração garante que a saída de uma pasta seja sempre a entrada exata da pasta seguinte).
