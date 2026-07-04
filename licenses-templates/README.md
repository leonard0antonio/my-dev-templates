# ⚖️ Templates de Licenças Open Source

Esta pasta contém templates pré-configurados das licenças open-source mais utilizadas no mercado. Todos os arquivos já estão preenchidos com os dados de autoria e ano corrente, prontos para serem anexados aos novos repositórios.

A escolha de uma licença é o que define legalmente como outras pessoas podem usar, modificar e distribuir o código dos projetos criados.

## 📂 Licenças Disponíveis

* [**`LICENSE-MIT`**](./LICENSE-MIT) 🟢
  * **Uso:** A mais permissiva e comum.
  * **O que permite:** Praticamente tudo (uso comercial, modificação, distribuição, código fechado).
  * **Exigência:** Manter o aviso de copyright original. Ideal para projetos que você quer que sejam usados o máximo possível.

* [**`LICENSE-APACHE`**](./LICENSE-APACHE) (Apache 2.0) 🟡
  * **Uso:** Muito comum em ambientes corporativos.
  * **O que permite:** Tudo o que a MIT permite, mas com uma cláusula forte de proteção contra processos por quebra de patentes.
  * **Exigência:** Manter os créditos e documentar se houve alterações no código original.

* [**`LICENSE-GPLv3`**](./LICENSE-GPLv3) (GNU GPLv3) 🔴
  * **Uso:** A licença "Copyleft" clássica para garantir que o software livre continue livre.
  * **O que permite:** Uso, modificação e distribuição comercial.
  * **Exigência:** Qualquer projeto derivado que for distribuído **obrigatoriamente** deve ter o código aberto sob a mesma licença GPLv3.

## 🚀 Como usar

1. Ao iniciar um novo projeto e decidir abri-lo para a comunidade, escolha qual licença se adequa melhor ao seu objetivo.
2. Copie o conteúdo do arquivo escolhido nesta pasta.
3. Crie um arquivo chamado **apenas `LICENSE`** (sem extensão `.md` ou `.txt`) na **raiz** do seu novo repositório.
4. Cole o texto dentro dele. O GitHub automaticamente reconhecerá a licença e adicionará um selo ao seu repositório!