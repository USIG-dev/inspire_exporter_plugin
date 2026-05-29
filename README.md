# INSPIRE Exporter

Esta versão exporta QMD e XML ISO 19139 orientado ao Perfil Nacional de Metadados de Informação Geográfica, Perfil MIG v2, de 8 Julho 2013.

O plugin gera a estrutura obrigatória para CDG/séries: identificação, palavras-chave GEMET/INSPIRE, restrições, categoria temática, resolução espacial, tipo de representação, extensão geográfica, distribuição, metadados, qualidade/histórico e sistema de referência.

Para conformidade semântica, preencha na camada QGIS as propriedades personalizadas aplicáveis:

- inspire/theme: código ou nome do tema INSPIRE, por exemplo au, cp, Unidades administrativas.
- inspire/topic_category: categoria ISO, por exemplo boundaries, planning Cadastre, transportation.
- inspire/identifier ou mig/resource_identifier: identificador do recurso.
- mig/file_identifier: UUID do documento de metadados; se vazio, o plugin gera um UUID estável.
- inspire/organisation, inspire/email, inspire/contact_name: contacto responsável.
- inspire/resource_language: por, eng ou zxx.
- inspire/lineage ou mig/lineage: histórico/linhagem.
- inspire/spatial_resolution_distance: distância de resolução em metros, se não usar escala.
- mig/distribution_format e mig/distribution_format_version: formato e versão de distribuição.
- mig/resource_locator: URL de acesso/descarga/pesquisa do recurso.
- mig/resource_locator_function: download, information, search ou order.
- inspire/access_constraints, inspire/use_constraints: códigos ISO como other restrictions,copyright, license.
- inspire/conditions: termos de acesso e uso.
- inspire/conformity_pass: true ou false quando a conformidade com a especificação INSPIRE foi avaliada.

Quando valores obrigatórios dependem do conhecimento do produtor e não estão na camada, o plugin cria INSPIRE_WARNINGS.txt na pasta de exportação.
