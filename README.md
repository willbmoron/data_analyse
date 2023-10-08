import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: LoginScreen(),
    );
  }
}

class LoginScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Rastreamento de Visualizações'),
      ),
      body: Padding(
        padding: const EdgeInsets.all(16.0),
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          crossAxisAlignment: CrossAxisAlignment.center,
          children: <Widget>[
            TextField(
              decoration: InputDecoration(
                labelText: 'Nome de Usuário',
              ),
            ),
            SizedBox(height: 16.0),
            TextField(
              obscureText: true,
              decoration: InputDecoration(
                labelText: 'Senha',
              ),
            ),
            SizedBox(height: 24.0),
            ElevatedButton(
              onPressed: () {
                // Coloque aqui a lógica para autenticar o usuário.
                // Você pode verificar as credenciais e redirecionar para a próxima tela.
              },
              child: Text('Entrar'),
            ),
            SizedBox(height: 8.0),
            TextButton(
              onPressed: () {
                // Coloque aqui a lógica para redefinir a senha, se necessário.
              },
              child: Text('Esqueceu a senha?'),
            ),
          ],
        ),
      ),
    );
  }
}
