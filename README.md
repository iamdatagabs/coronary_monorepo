# Coronary Monorepo
## Predição de doença coronariana e desfechos cardiovasculares — especificação de pesquisa

**Portfólio:** [Gabriel Passos](https://iamdatagabs.github.io/iamdatagabs/portfolio/) · **GitHub:** [iamdatagabs/coronary_monorepo](https://github.com/iamdatagabs/coronary_monorepo)

## Sobre

Este repositório documenta a proposta metodológica e a arquitetura de um estudo retrospectivo e experimental para investigar fatores associados à doença coronariana e comparar abordagens estatísticas e de aprendizado de máquina em uma base pública/didática.

A proposta combina estatística inferencial, avaliação de modelos preditivos, métricas de acurácia diagnóstica e técnicas de explicabilidade. **O repositório ainda não contém a implementação executável do pipeline descrito abaixo**: no estado atual, reúne esta documentação e o esboço de estrutura em [architecture/estrutura](architecture/estrutura).

## Pergunta analítica

Como diferentes abordagens estatísticas e de machine learning se comparam na discriminação e calibração de um desfecho binário relacionado à doença coronariana, considerando interpretabilidade e métricas relevantes para avaliação diagnóstica?

## Base de dados planejada

- Heart Attack Analysis & Prediction Dataset, de circulação pública em repositórios educacionais como Kaggle.
- A descrição preliminar prevê uma amostra de 303 registros, 13 variáveis preditoras e um desfecho binário.
- A origem exata, versão, licença, dicionário de dados, critérios de inclusão e qualidade dos registros deverão ser verificados antes da implementação e de qualquer análise.

A disponibilidade pública de uma base não garante qualidade clínica, representatividade ou adequação para inferência sobre outras populações.

## Plano metodológico proposto

1. **Caracterização da amostra:** descrição das variáveis, dados ausentes, distribuições e consistência semântica.
2. **Estatística inferencial:** comparação entre grupos com métodos adequados ao tipo e à distribuição das variáveis; estimativas de associação com intervalos de confiança.
3. **Modelagem:** comparação planejada entre regressão logística penalizada, Random Forest, XGBoost e LightGBM.
4. **Avaliação:** validação cruzada estratificada, AUROC, AUPRC, Brier Score, calibração, sensibilidade, especificidade, VPP, VPN e razões de verossimilhança.
5. **Utilidade e explicabilidade:** análise de curva de decisão e SHAP, com atenção à estabilidade e às limitações de interpretação.

Essas etapas são um plano metodológico, não resultados já executados. A estratégia de validação, seleção de limiar, tratamento de dados ausentes e prevenção de vazamento deverá ser definida antes da análise.

## Estrutura planejada

A estrutura proposta está descrita em [architecture/estrutura](architecture/estrutura) e prevê módulos separados para configuração, estatística, modelagem, métricas e visualização. A implementação futura deverá incluir testes, ambiente reproduzível, documentação de dados e registro de experimentos.

## Próximos passos

- [ ] Confirmar fonte, licença, versão e dicionário da base.
- [ ] Implementar ingestão, validação e análise exploratória.
- [ ] Criar protocolo de divisão dos dados e validação sem vazamento.
- [ ] Implementar os métodos estatísticos e modelos planejados.
- [ ] Adicionar testes automatizados e configuração de ambiente.
- [ ] Registrar métricas, incerteza, análise de erros e limitações.
- [ ] Documentar a reprodutibilidade e atualizar este README após resultados efetivamente obtidos.

## Limitações e uso responsável

Este é um projeto de pesquisa/estudo metodológico com dados públicos ou educacionais. Não é um modelo clínico validado, não estima risco individual de pacientes e não deve orientar diagnóstico, tratamento, triagem ou qualquer decisão assistencial. Métricas obtidas em bases didáticas não demonstram validade externa, utilidade clínica ou desempenho em populações reais.

Nenhum dado identificável de pacientes deve ser incluído no repositório. Qualquer futura utilização de dados clínicos exige base legal, aprovação ética quando aplicável, governança, minimização e salvaguardas adequadas.

## Licença

Consulte o arquivo [LICENSE](LICENSE). A licença do código não substitui os termos de uso e redistribuição da base de dados, que devem ser verificados separadamente.
