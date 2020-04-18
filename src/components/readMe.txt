component general structure:

import React, { Component } from 'react';
import axios from 'axios';
import DatePicker from 'react-datepicker';
import "react-datepicker/dist/react-datepicker.css";
export default class CreateExercise extends Component {

  constructor(props) {
     super(props);

     this.<EventName> = this.<EventName>.bind(this);

     this.state = {
         //initialization of the data models
        }
    }

  componentDidMount() {
        /*
        It is called once in the component life cycle and it signals that the component and all its sub-components
        have rendered properly. This is the best place to make API calls since, at this point, the component has been
        mounted and is available to the DOM.
        */
  }

  <Event>(e) {
          this.setState({
              <dataElement>: e.target.value
          })
      }

  onSubmit(e) {
          e.preventDefault();

          const <DataCollectionName> = {
              <dataElement>: this.state.<dataElement>,
          }

  axios.post('http://localhost:5000/<DataCollectionNameUsedInThePostRequests>/<Operation>', <DataCollectionName>)
              .then(res => console.log(res.data));

  render() {
    //JSX code here
  }

}