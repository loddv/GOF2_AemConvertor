### AemConvertor
Um script Python simples para converter ficheiros .aem para .obj ou .obj para .aem. Basta arrastar um ficheiro ou caminho para a janela do script e pressionar Enter para iniciar a conversão.
Funcionalidades na Versão Mais Recente
Aem2obj (AEM para OBJ)
 * Conversão: Converte o ficheiro .aem no ficheiro .obj, incluindo informação de vértices, UVs, normais e faces.
 * Nota: Todas as faces serão isoladas devido à estrutura de dados dos ficheiros .aem.
Obj2aem (OBJ para AEM)
 * Conversão: Converte o ficheiro .obj no formato .aem. Os dados de vértices, UVs, normais e faces devem estar incluídos no ficheiro .obj para que a conversão seja bem-sucedida.
 * Limitação de Tamanho: O formato AEM não permite mais de 65535 vértices num único ficheiro. No entanto, foi implementado um método que utiliza "fragmentos" para estender este limite até 4.294.836.225 vértices, o que significa um máximo de 1.431.612.075 faces no ficheiro .obj.
 * Requisito: Certifique-se de que o ficheiro .obj a ser convertido tem dados suficientes e não é demasiado grande antes de converter.
Aviso
 * Existem alguns bytes desconhecidos no ficheiro .aem que são preenchidos com '00' durante a conversão de OBJ. Isto pode causar efeitos secundários. Por favor, relate se encontrar erros.
Instruções de Uso
Requisitos
 * Python (para executar o script aemconvertor.py).
 * O script aemconvertor.py.
 * Os modelos .aem (geralmente localizados em data/assets/main/3d/meshes/ships) ou os seus modelos .obj modificados.
Método 1: Arrastar e Soltar (Mais Simples)
 * Localize o ficheiro aemconvertor.py no seu explorador de ficheiros.
 * Arraste o ficheiro de modelo (.aem ou .obj) que deseja converter e solte-o no ícone do script aemconvertor.py.
 * O script será iniciado e converterá o ficheiro.
Método 2: Linha de Comando (Recomendado para Usuários Avançados)
 * Abra o CMD ou Powershell na pasta onde se encontra o script aemconvertor.py.
 * Utilize o seguinte comando, substituindo [nome_do_ficheiro] pelo nome do ficheiro que pretende converter:
   Para converter de AEM para OBJ:
   python .\aemconvertor.py [nome_do_ficheiro].aem
#### Exemplo: python .\aemconvertor.py ship_001_terran.aem
##### O resultado será um novo ficheiro .obj na mesma pasta.

   Para converter de OBJ para AEM:
   python .\aemconvertor.py [nome_do_ficheiro].obj
#### Exemplo: python .\aemconvertor.py minha_nave_modificada.obj
###### O resultado será um novo ficheiro .aem na mesma pasta.

