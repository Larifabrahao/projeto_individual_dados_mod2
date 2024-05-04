## **Projeto Individual - Date Analytics**
_Projeto Individual do Módulo 02 - Programadores Cariocas 2024_

<br><br>

# **_Sistema RESILIADATA_**

## _PROPOSTA DO TRABALHO: <br>_
Você foi contratado para desenvolver um banco de dados que irá armazenar dados
importantes que será utilizado pelo sistema RESILIADATA.
  + O sistema irá auxiliar na avaliação de quais são as tecnologias que as empresas parceiras
estão utilizando e quem são seus colaboradores; <br>
  + Vamos ter o cadastro de empresas parceiras, cadastro de tecnologias com a opção de
selecionar a área (webdev, dados, marketing, etc.), uma tabela para registrar quais
tecnologias as empresas estão utilizando e uma tabela para cadastro de colaboradores.
<br><br><br>


## _PERGUNTAS: <br>_
**1. Quais são as entidades necessárias? <br>**
   Empresa Parceira, Tecnologia e Colaborador
<br><br><br>

   
**2. Quais são os principais campos e seus respectivos tipos?**
   * Empresa Parceira:
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * CNPJ (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * Endereço (varchar - String/Texto de tamanho variável com limite)
     * Telefone (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     
   * Tecnologia:
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * Área (varchar - String/Texto de tamanho variável com limite)
     
   * Colaborador:
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * CPF (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * Cargo (varchar - String/Texto de tamanho variável com limite)
     * Telefone (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * ID_Empresa Parceira (int - Inteiro, chave estrangeira referenciando a tabela Empresa Parceira)
     * ID_Tecnologia (int - Inteiro, chave estrangeira referenciando a tabela Tecnologia)
<br><br><br>


**3. Como essas entidades estão relacionadas?**
   * Empresa Parceira - Tecnologia = 1:N <br>
     Uma Empresa Parceira pode estar associada a várias Tecnologias, portanto é uma relação de "uma para muitas".
     
   * Colaborador - Tecnologia = N:N <br>
     Apesar de um Colaborador só poder estar associado a uma Empresa Parceira, ele pode possuir conhecimento em várias Tecnologias. Esse é um relacionamento de "muitos para muitos", onde múltiplos colaboradores podem ter conhecimento em múltiplas tecnologias.
     
   * Empresa Parceira - Colaborador = 1:N <br>
     Um Colaborador pode estar associado a/trabalha para apenas uma Empresa Parceira. Esse é um relacionamento de "uma para muitos", onde uma empresa pode ter vários colaboradores, mas um colaborador está associado a apenas uma empresa.
<br><br><br>


**4. Simule 2 registros para cada entidade. <br>**
