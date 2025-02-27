import React, { useState } from 'react';
import { View, Text, TextInput, Button, StyleSheet } from 'react-native';

const App = () => {
  const [fecha, setFecha] = useState('');
  const [operador, setOperador] = useState('');
  const [entidad, setEntidad] = useState('');

  const handleSave = () => {
    // Aquí iría la lógica para guardar los datos
    console.log('Datos Guardados:', { fecha, operador, entidad });
  };

  return (
    <View style={styles.container}>
      <Text style={styles.header}>Datos Básicos</Text>
      <TextInput
        style={styles.input}
        placeholder="Fecha"
        value={fecha}
        onChangeText={setFecha}
      />
      <TextInput
        style={styles.input}
        placeholder="Operador"
        value={operador}
        onChangeText={setOperador}
      />
      <TextInput
        style={styles.input}
        placeholder="Entidad"
        value={entidad}
        onChangeText={setEntidad}
      />
      <Button title="Guardar" onPress={handleSave} />
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    padding: 20,
    backgroundColor: '#fff',
  },
  header: {
    fontSize: 24,
    fontWeight: 'bold',
    marginBottom: 20,
  },
  input: {
    height: 40,
    borderColor: 'gray',
    borderWidth: 1,
    marginBottom: 20,
    paddingHorizontal: 10,
  },
});

export default App;
