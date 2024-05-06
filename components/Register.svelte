<script>
  let email = '';
  let password = '';
  let confirmPassword = '';

  const handleRegister = () => {
    // Verifica se a senha e a confirmação da senha correspondem
    if (password !== confirmPassword) {
      alert("A senha e a confirmação da senha não correspondem.");
      return;
    }
    
    // Aqui você pode adicionar a lógica para registrar o usuário
    console.log('Email:', email);
    console.log('Password:', password);
    console.log('Confirm Password:', confirmPassword);
  };
</script>

<style>
  /* Adicione os estilos CSS necessários para o design anterior */
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-image: url('seu_banner.jpg'); /* Substitua 'seu_banner.jpg' pelo caminho da sua imagem de banner */
    background-size: cover;
  }

  form {
    background-color: rgba(255, 255, 255, 0.8);
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
    background-color: #007bff;
    color: #fff;
    cursor: pointer;
  }
</style>

<div class="container">
  <div>
    <h2>Register</h2>
    <form on:submit|preventDefault="{handleRegister}">
      <label>
        Email:
        <input type="email" bind:value="{email}" required />
      </label>
      <label>
        Password:
        <input type="password" bind:value="{password}" required />
      </label>
      <label>
        Confirm Password:
        <input type="password" bind:value="{confirmPassword}" required />
      </label>
      <button type="submit">Register</button>
    </form>
  </div>
</div>
