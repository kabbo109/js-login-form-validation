function validate(){
  const email = document.getElementById('email').value;
  const pass = document.getElementById('password').value;
  const msg = document.getElementById('msg');

  const emailValid = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);

  if(!emailValid){
    msg.innerText = 'Invalid email address';
    msg.style.color = 'red';
  }else if(pass.length < 6){
    msg.innerText = 'Password must be at least 6 characters';
    msg.style.color = 'orange';
  }else{
    msg.innerText = 'Login successful ✔';
    msg.style.color = 'lightgreen';
  }
}
