# ozariasValidation

jQuery.ozariasValidation v1.0

Atende qualquer tipo de validação de formulário.

Simples e prático, pra validar qualquer campo do formulário.

Valida campos obrigatórios, expressões regulares, e também é possivel criar funções personalizadas.
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js" type="text/javascript"></script>
<script src="js/bootstrap.min.js" type="text/javascript"></script>
<script src="js/ozariasValidation-1.0.js" type="text/javascript"></script>
Exemplo de validação simples
<script type="text/javascript">
  $(document).ready(function(){
    // event de submit
    $("#formValidator2").submit(function(e){         
     // Cancela o evento
      e.preventDefault();          

      var validaForm = $(this).find("#validator2").ozariasValidation({language:"pt-br"});
      if(validaForm.validateForm()){                         
         alert("Validou");
      }
    })
  })
</script>
<form method="post" style="margin: 50px 0" id="formValidator2">  
  <div id="validator2">
    <div class="form-group">
      <label>Nome <span class="label label-danger">required</span></label>
      <input data-labelname="Nome" id="nome" name="nome" aria-describedby="inputSuccess2Status" class="form-control validate[required]" placeholder="Seu nome" type="text">                        
    </div>

    <div class="form-group">
      <label for="">Email <span class="label label-danger">required regex</span></label>
      <input data-labelname="Email" type="text" id="email" name="email" class="form-control validate[required, regex[email]]" placeholder="email" >
    </div>

    <div class="form-group">
      <label for="">Confirmação de Email <span class="label label-danger">confirmation</span></label>
      <input data-labelname="Confirmação de Email" type="text" id="cmeial" name="cemail" class="form-control validate[confirm[email]]" placeholder="confirmação do email" >
    </div>                  
  </div>    
  <button type="submit" class="btn brn-default">Validar</button>
</form> 


Documentação no link https://rogerio-ozarias.github.io/ozariasValidation
