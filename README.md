# Escrevendo-no-Celular
### Repositório para criar os casos de teste da questão do DojoPuzzles "Escrevendo no Celular" 
  * Membros: Alan David, Lucas de Lima
  * Problema: [link](http://dojopuzzles.com/problemas/exibe/escrevendo-no-celular/)
  * Tecnologia: Php com Laravel 5.4
  
  
  ## Plano de teste

| Entrada  | Condição | Classes Válidas | Classes Inválidas |
| ------------- | ------------- | ------------- | ------------- |
| Cadeia de Caracteres      |Cadeia Igual à string  | is_string($cadeia) == True | is_string($cadeia) != True |
| Cadeia de Caracteres      |Cadeia Menor ou Igual à 255 Caracteres | strlen ( string $cadeia ) <= 255 | strlen ( string $cadeia ) > 255 |
| Cadeia de Caracteres      |Cadeia ser diferente de vazia  | strlen > 0 | strlen <= 0  |

 ### Protótipos dos métodos

```php
asciiToGSM(String $cadeia)
```

### 1º Caso de Teste

```php
asciiToGSM("a") // Retorna a Cadeia de numeros "1"
```

### 2º Caso de Teste

```php
asciiToGSM(1) // Retorna UnexpectedValueException
```

### 3º Caso de Teste

```php
asciiToGSM("Gol de mao") // Retorna a Cadeia de numeros "46665550333062666"
```

### 4º Caso de Teste

```php
asciiToGSM("") // Retorna UnexpectedValueException
```

## 5º Caso de Teste 

```php
asciiToGSM("Por conseguinte, a constante divulgação das informações nos obriga à análise do processo de comunicação como um todo. Evidentemente, a complexidade dos estudos efetuados faz parte de um processo de gerenciamento dos métodos utilizados na avaliação de resultados.") // Retorna UnexpectedValueException
```
