SimpleImage
===========

SimpleImage, e uma classe criada com o intuito de facilitar a manipula��o de imagens no php.


Exemplo
-------

	require 'SimpleImage/SimpleImage.php';
	
	$simple = new SimpleImage('../imagem/teste.png');
	
Fun��es
-------

	// rotaciona a imagem 90� sentido anti-horario
	$simple->rotate90();
	
	// rotaciona a imagem 180� sentido anti-horario
	$simple->rotate180();
	
	// rotaciona a imagem 270� sentido anti-horario
	$simple->rotate270();
	
	// muda o tipo da imagem para gif
	$simple->cloneToGIF();
	
	// muda o tipo da imagem para png
	$simple->cloneToPNG();
	
	// muda o tipo da imagem para jpeg
	$simple->cloneToJPEG();
	
	// corta uma parte da imagem, de acordo com os par�metros passado
	$simple->crop($width, $height, $percToRight, $percToBottom);
	
	// redimensiona a imagem, para os novos par�metros informados
	$simple->resize($newWidth, $newHeigth);
	
	// redimensiona a imagem, para os novos par�metros informados proporcionalmente
	$simple->resizeProportional($newWidth, $newHeigth);
	
	// copia uma imagem para outra, informando a posi��o da sobreposi��o
	$simple->merge('../imagem/nova.gif', $percToRight, $percToBottom);
	
	// retorna a altura da imagem
	$simple->getHeight();
	
	// retorna a largura da imagem
	$simple->getWidth();
	
	// retorna o tamanho da imagem
	$simple->getSize();
	
	// retorna o tipo da imagem
	$simple->getType();
	
	// retorna o caminho da imagem
	$simple->getFile();
	
	// escreve na imagem
	* necess�rio setar a fonte primeiro
	$simple->write($texto, $percToRight, $percToBottom);
	
	// setar a fonte que ser� usada durante a escrita
	$simple->setFont($caminho);
	
	// seta a cor da fonte
	$simple->setFontColor($hexadecimal);
	
	// seta o tamanho da fonte
	$simple->setFontSize($size);
	
	// salva imagem, caso n�o seja informado o nome, ele gera um hash e salva
	$simple->save();
	
	
Observa��es
-----------

Atualmente a classe so trabalha com 3 tipos de imagem, PNG, JPEG e GIF.

	
	