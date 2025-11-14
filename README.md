Sistema de Gestão de Horas Extras (Base27) 

Descrição:
Este projeto implementa um sistema completo de solicitação, cálculo e aprovação de horas extras, inspirado em regras comuns de jornada de trabalho e adicional noturno.
O sistema é voltado para uso em terminal e foi personalizado com elementos visuais, tabela estruturada, logo da Base27, animações simples e um fluxo completo de funcionário e gestor.

Funcionalidades Principais
1. Registro Automático das Solicitações
Cada solicitação é salva em solicitacoes.csv, contendo:
ID
Nome
Salário
Horas trabalhadas
Horas extras solicitadas
Tipo(diurna/noturna)
Status (pendente, aprovado ou negado)
Motivo
Valor estimado

O sistema também mantém um histórico mensal, renomeando automaticamente o CSV ao mudar o mês.

2. Cálculos Implementados
Horas trabalhadas: calculadas considerando virada de dia.
Horas extras:
Hora extra diurna: +50%.
Hora extra noturna: adicional +25% sobre o extra (1.5 × 1.25).

3. Detecção automática de extra noturna:
Considera como período noturno o intervalo entre 22:00 e 05:00.

4. Fluxo do Funcionário
Informa ID e nome.
O sistema tenta identificar salário automaticamente pelo ID.
Caso não exista, o salário é solicitado e salvo nas próximas requisições.
Informa horários de início, fim e próxima jornada.
Informa horas extras desejadas.
Solicitação é enviada ao gestor.

5. Fluxo do Gestor
Acesso mediante senha.
Visualização das solicitações pendentes em tabela formatada.
Possibilidade de aprovar ou negar cada solicitação.
Atualização automática do CSV.

6. Observações Importantes:
Senha do gestor: admin;
O sistema cria automaticamente o arquivo solicitacoes.csv se ele não existir;
O histórico é gerado sempre que o mês muda.
