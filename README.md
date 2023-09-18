# README DA ATIVIDADE DE LP DAS MÚSICAS
README do jogo feito com a ferramenta Unity para a matéria de Linguagem de Programação, onde foram escolhidos duas músicas e fazer duas cenas baseada em ambas.
## COMO É O JOGO?
O jogo é 3D mas com a jogabilidade de um jogo de plataforma, onde se movimenta o personagem apenas para cima e para baixo. O jogo conta a história de um capitão que perdeu sua tripulação por causa da raiva e egoismo.
## MÚSICAS ESCOLHIDAS
O Limbo do Menino Sem Olhos e Moby Dick, ambas do cantor Kamaitachi.

## DOCUMENTAÇÃO E DIAGRAMA DE CASOS E DIAGRAMA DE CLASSES
Diagrama de Casos de Uso
<br><img src="img/usecasediagram.png">

Diagrama de Classe
<br><img src="img/classdiagram.png">

Documentação do Caso de Uso
<br><img src="img/usecase.png">

Documentação do Diagrama de Classes
<br><img src="img/class.png">

## O desenvolvimento

![Cena 1 (OCM)](https://github.com/yuritelis/atvmusicalp/assets/127852225/359f6b0e-24a4-4584-af9e-fe1d15caf55b)<br>
O objetivo deste jogo era criar uma transição de cenários, de uma fase para a outra. Começamos do básico, criamos a primeira cena e começamos a modelar as coisas com base nas músicas escolhidas. A maioria dos objetos foi obtida na Unity Store (o link dos Assets usados está logo abaixo). Utilizamos assets de um barco, piratas, uma rocha e o mar, e montamos toda a primeira cena.

O propósito da primeira cena era apresentar a parte da história, mostrando uma briga que estava ocorrendo no navio, que posteriormente afundaria. Na segunda cena, utilizamos a maior parte dos assets da primeira cena, incorporando também alguns GameObjects básicos do Unity. A segunda cena é onde o jogo realmente começa, pois é onde o gênero "Plataforma" se aplica, apresentando um cenário em 3D, mas com o jogador movendo-se como em um jogo de plataforma. O objetivo é atravessar um percurso e chegar ao baú do tesouro sem cair no mar, enquanto o "monstro do mar" permanece observando no fundo.<br>
## Print da Cena 2
![Cena 2 (OCM)](https://github.com/yuritelis/atvmusicalp/assets/127852225/afb98124-d02d-4022-8dbb-47818ff20880)

## Personagens 
![Personagens e Barcos (OCM)](https://github.com/yuritelis/atvmusicalp/assets/127852225/913c1d4f-8b5c-4bb7-b01d-c5be8bdeee90)<br>
Os personagens, como mencionado anteriormente, foram adquiridos na Unity Asset Store. Neste jogo, estamos experimentando a perspectiva do Capitão em relação à história. Na primeira cena, o personagem pode se movimentar livremente pelo barco, enquanto na segunda cena ele se move apenas nos eixos x e y. Para alcançar isso, utilizamos dois scripts diferentes: um que utiliza todos os eixos e outro que utiliza apenas dois eixos.<br>
Movimento em todos eixos:<br>

    void Update()
    {
        
       if (Input.GetKey (KeyCode.W)) {
            transform.Translate(-0.06f, 0f,0f); } 
       if (Input.GetKey (KeyCode.S)) {
             transform.Translate(0.06f,0f,0f); }
       if (Input.GetKey (KeyCode.D)) {
           transform.Translate(0.0f,0f,0.06f); } 
       if (Input.GetKey (KeyCode.A)) {
           transform.Translate(0.0f,0f,-0.06f); } 
       if (Input.GetKey (KeyCode.Space)) {
           transform.Translate(0.0f,0.03f,0f); } 

        bool isLeftButtonDown = Input.GetMouseButtonDown (0);
        bool isRightButtonDown = Input.GetMouseButtonDown (1);
        bool isMiddleButtonDown = Input.GetMouseButtonDown (2);
            print (isLeftButtonDown);

Movimento nos eixos X e Y:

     if (Input.GetKey(KeyCode.D)) { 
			transform.Translate(0f, 0f, 2f); }//Movimentação para direita 
		if (Input.GetKey(KeyCode.A)) { 
			transform.Translate(0f, 0f, -2f); }//Movimentação para esquerda
        if (Input.GetKey (KeyCode.Space)) {
			transform.Translate(0f, 6f, 0f); }//Botao de Pulo

Se quiser saber mais sobre a movimentação e as coisas mais básicas em um repositório, você pode clicar [aqui](https://github.com/KauanJesusJD/Broto-Mortal).

## A transicao de Cena e os textos
![Textos e Button (OCM)](https://github.com/yuritelis/atvmusicalp/assets/127852225/abbd9104-cbcd-4f98-8140-d8f65d98d748)<br>
A ideia original era criar interações e diálogos, mas devido a vários imprevistos, acabamos usando o canvas do Unity para exibir os textos.

Quanto à troca de cena, realizamos uma pesquisa sobre como fazê-la e optamos por utilizar um GameObject "Button" do Canvas. Desenvolvemos um código de script para executar a troca de cena e vinculamos esse código à função "Onclick()" do Button.

      using System.Collections;
      using System.Collections.Generic;
      using UnityEngine;
      using UnityEngine.SceneManagement;

    public class Trocarcena : MonoBehaviour
    {
    
	public void Jogar()
	{
		SceneManager.LoadScene(1);
	}
    
    }

Para obter mais informações sobre como realizar a troca de cena, clique neste [link](https://www.youtube.com/watch?v=9cVs70Wzzo8) de um vídeo que utilizamos como referência. para essa tarefa.

## Link do Jogo(Compactado)<br>
https://drive.google.com/drive/folders/1zAcVHowSYLEl2dQfXSywRGQvgS540PoF?usp=drive_link


## AUTORES
Kauan Jesus e Yuri Telis.
