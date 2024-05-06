<script>
  let email = '';
  let password = '';

  const handleLogin = () => {
    // Aqui você pode adicionar a lógica para autenticação do usuário
    console.log('Email:', email);
    console.log('Password:', password);
  };
</script>

<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-image: url('seu_banner.jpg'); /* Adicione o caminho da sua imagem de banner */
    background-size: cover;
  }

  form {
    background-color: rgba(255, 255, 255, 0.8); /* Adiciona um fundo branco transparente ao formulário */
    padding: 20px;
    border-radius: 10px;
  }

  label {
    display: block;
    margin-bottom: 10px;
  }

  input {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
  }

  button {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: #007bff; /* Altera a cor de fundo do botão para azul */
    color: #fff; /* Altera a cor do texto do botão para branco */
    cursor: pointer;
  }
</style>

<div class="container">
  <div>
    <h2>Login</h2>
    <form on:submit|preventDefault="{handleLogin}">
      <label>
        Email:
        <input type="email" bind:value="{email}" required />
      </label>
      <label>
        Password:
        <input type="password" bind:value="{password}" required />
      </label>
      <button type="submit">Login</button>
    </form>
  </div>
</div>
