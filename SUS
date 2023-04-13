import { StatusBar } from "expo-status-bar";
import {
  Alert,
  StyleSheet,
  Text,
  TextInput,
  View,
  Button,
  FlatList,
  TouchableOpacity,
  ScrollView,
} from "react-native";
import React, { useState } from "react";
import { AntDesign } from "@expo/vector-icons";
import { MaterialCommunityIcons } from "@expo/vector-icons";
import { Ionicons } from "@expo/vector-icons";

export default function App() {
  const [nome, setNome] = useState(" ");
  const [esp, setEsp] = useState([
    { esp: "Ortopedia", key: 1 },
    { esp: "Clinica Geral", key: 2 },
    { esp: "Dermatologia", key: 3 },
    { esp: "Pediatria", key: 4 },
    { esp: "Cardiologia", key: 5 },
    { esp: "Nefrologia", key: 6 },
    { esp: "Oftamologia", key: 7 },
    { esp: "Oncologia", key: 8 },
    { esp: "Pneumologia", key: 9 },
    { esp: "Geriatria", key: 10 },
    { esp: "Neurologia", key: 11 },
    { esp: "Alergologia", key: 12 },
  ]);
  const [agenda, setAgenda] = useState([
    { ag: "Consultas 🗓️", key: 13 },
    { ag: "Exames 🔬", key: 14 },
    { ag: "Medicação 💊", key: 15 },
    { ag: "Vacinas 💉", key: 16 },
  ]);
  return (
    <View style={styles.container}>
      <View>
        <Text style={styles.texto}> Meu Doutor 🩺 </Text>
      </View>

      <View style={styles.blocologin}>
        <Text style={styles.texto2}>Olá {nome}!Faça seu login</Text>
        <View style={styles.boxnome}>
          <View>
            <AntDesign name="user" size={22} color="black" />
          </View>
          <View>
            <TextInput
              multiline
              style={styles.input}
              placeholder="Digite seu nome"
              onChangeText={setNome}
            />
          </View>
        </View>
        <View style={styles.boxsenha}>
          <View>
            <MaterialCommunityIcons
              name="eye-off-outline"
              size={22}
              color="black"
            />
          </View>
          <View>
            <TextInput
              multiline
              style={styles.input2}
              placeholder="Digite sua Senha"
              keyboard=""
            />
          </View>
        </View>

        <View style={styles.botao}>
          <Button
            title="continuar"
            onPress={() => Alert.alert("Você está logado!")}
          />
        </View>
      </View>
      <View style={styles.marcacao}>
        <ScrollView>
          {agenda.map((itens) => {
            return (
              <View key={itens.key}>
                <TouchableOpacity>
                  <Text style={styles.itens}>{itens.ag}</Text>
                </TouchableOpacity>
              </View>
            );
          })}
        </ScrollView>
      </View>

      <View style={styles.busca}>
        <View>
          <Ionicons name="search" size={20} color="black" />
        </View>
        <View>
          <TextInput
            style={styles.input3}
            placeholder="Busque por especialidade"
          />
        </View>
      </View>

      <View style={styles.menu}>
        <FlatList
          numColumns={2}
          keyExtractor={(item) => item.key}
          data={esp}
          renderItem={({ item }) => (
            <TouchableOpacity>
              <Text style={styles.item}>{item.esp}</Text>
            </TouchableOpacity>
          )}
        />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: "#fff",
    alignItems: "center",
    justifyContent: "flex-start",
    backgroundColor: "#C5DBFD",
    padding: 35,
    marginTop: 20,
  },

  blocologin: {
    backgroundColor: "#FFFF99",
    borderRadius: 10,
    marginTop: 8,
    padding: 20,
    borderWidth: 2,
  },
  texto: {
    backgroundColor: "#FFFF99",
    fontSize: 45,
    color: "blue",
    borderRadius: 10,
    borderWidth: 2,
  },
  texto2: {
    backgroundColor: "#FFFF99",
    fontSize: 20,
    borderRadius: 10,
    marginTop: 2,

    color: "blue",
  },
  input: {
    backgroundColor: "white",
    borderRadius: 10,
    borderWidth: 2,
    marginTop: 15,
    fontSize: 15,
  },
  input2: {
    backgroundColor: "white",
    borderRadius: 10,
    borderWidth: 2,
    marginTop: 15,
    fontSize: 15,
  },

  botao: {
    marginTop: 15,
  },

  boxnome: {
    flexDirection: "row",
    alignItems: "center",
  },
  boxsenha: {
    flexDirection: "row",
    alignItems: "center",
  },
  input3: {
    backgroundColor: "white",
    borderRadius: 10,
    borderWidth: 1,
    marginTop: 15,
    padding: 15,
  },
  busca: {
    flexDirection: "row-reverse",
    alignItems: "center",
    backgroundColor: "#FFFF99",
    marginTop: 10,
    borderRadius: 10,
    padding: 6,
    borderWidth: 2,
  },
  item: {
    flex: 1,
    backgroundColor: "blue",
    borderRadius: 10,
    borderWidth: 2,
    fontSize: 12,
    padding: 21,
    marginTop: 20,
    width: "98%",
    marginLeft: 30,
    marginRight: 8,
    color: "white",
    borderColor: "black",
  },
  menu: {
    flex: 1,
    flexDirection: "row",
    justifyContent: "space-evenly",
  },
  itens: {
    backgroundColor: "blue",
    borderRadius: 10,
    borderWidth: 2,
    color: "white",
    padding: 15,
    fontSize: 20,
  },
  marcacao: {
    marginTop: 10,
    flex: 1,
    padding: 10,
  },
});
