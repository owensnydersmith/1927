// Button consist two props: title and onPress

import React from 'react';
import { View, Alert, Button, Text, StyleSheet } from 'react-native';

async function fetchSensors(){
  console.log('fetchSensors')
  var url= 'https://bot3.seattleacademy.software/sensors';
  let response = await fetch(url);

if (response.ok) { // if HTTP-status is 200-299
  // get the response body (the method explained below)
  let json = await response.json();
  console.log(json.voltage);
} else {
  console.log("HTTP-Error: " + response.status);
}
}

export default class HandlingTouchesComponent extends React.Component {
  _onPress() {
    Alert.alert('Click a button');
  }
   _onPress1() {
    fetch('https://bot3.seattleacademy.software/sing?song=[90,10],[0,10],[90,10],[0,10],[90,10],[0,10],[90,10]')
  }
     _onPress2() {
    fetch('https://bot3.seattleacademy.software/drive?left=0&right=0')
  }
       _onPress3() {
    fetch('https://bot3.seattleacademy.software/drive?left=200&right=200')
  }
        _onPress4() {
    fetch('https://bot3.seattleacademy.software/drive?left=-100&right=-100')
  }
          _onPress5() {
    fetch('https://bot3.seattleacademy.software/drive?left=-100&right=100')
  }
      _onPress6() {
    fetch('https://bot3.seattleacademy.software/drive?left=100&right=-100')
  }
      _onPress7() {
        fetch('https://bot3.seattleacademy.software/drive?left=500&right=500')
  }



  render() {
    return (
      <View style= {
        styles.container
        }>
        <View style= {styles.button}>
          <Button
            title='Ping'  
            onPress={this._onPress1}  
          />
        </View>
        <View style= {styles.button}>
          <Button
          title= 'Turbo'
          onPress={this._onPress7} />
        </View>
        <View style= {styles.button}>
          <Button
            title='Forward' 
            onPress={this._onPress3}
          />
        <View style= {styles.containerButton}>
          <Button 
            title='Left'
            onPress={this._onPress6}
          />
           <Button 
            title='Stop' 
            onPress={this._onPress2}
          />
          <Button 
            title='Right'
            onPress={this._onPress5}
          />
        </View>
        <View style= {styles.button}>
          <Button
            title='Reverse'
            onPress={this._onPress4}
          />
        </View>
        <Text style= {styles.sensors}>
          Robot Battery Voltage: ...
        </Text>
      </View>
    </View>
    );
  }
}

const styles = StyleSheet.create({
    container: {
      flex: 0.8,
      justifyContent: 'center',
    },
    containerButton: {
      flexDirection: 'row',
      flex: 1,
      justifyContent: 'space-around',
    },
    button: {
      flex: 1,
      justifyContent: 'space-around',
    },
    sensors: {
      justifyContent: 'center',
    }
});
