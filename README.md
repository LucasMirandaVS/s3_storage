# Backup de Arquivos Locais para o S3

Sistema automatizado de backup utilizando Python e o serviço de armazenamento de objetos Amazon S3. O programa será responsável por ler arquivos de uma pasta local no seu computador, enviar esses arquivos para um bucket S3 na AWS e, em seguida, deletar os arquivos locais após o upload bem-sucedido.

## Fluxo
1 - Início do Backup: O processo começa com a execução do script Python.

2 - Listar Arquivos na Pasta Local: O script verifica a presença de arquivos na pasta local especificada.
Se arquivos forem encontrados, o processo continua.
Se nenhum arquivo for encontrado, o processo termina.

3 - Upload dos Arquivos para S3: Os arquivos listados são enviados para o bucket S3 designado.

4 - Upload Bem-Sucedido?: Verifica se o upload dos arquivos foi realizado com sucesso.
Se o upload for bem-sucedido, os arquivos locais são deletados.
Se ocorrer algum erro durante o upload, o erro é registrado para análise posterior.

5 - Fim do Processo: O processo de backup é concluído, seja após o upload e deleção dos arquivos ou após a detecção de um erro.