<template>
    <section>
      <h3>Add teacher</h3>
  
        <div><label for="">Nombre:</label><input type="text" v-model="teacher.teacherName"></div>
        <div><label for="">Apellido</label><input type="text" v-model="teacher.surname"></div>
        <div><label for="">DNI</label><input type="text" v-model="teacher.dni"></div>
        <div><label for="">Materias</label><input type="text" v-model="subject">
          <button v-on:click="handleSubject">Add materias</button>
        </div>
        <ul>
          <li v-for="(elm, index) in teacher.subjects" :key="index">{{  elm }}</li>
        </ul>
        <div><label for="">Docs </label><input type="checkbox" v-model="teacher.doc"></div>
        <button mat-button @click="handAddTeacher()">Add teacher</button>
  
  
  
    </section>
  
    <section>
  <h3>teacher list</h3>
  <table>
    <tr>
      <th>Nombre</th>
      <th>Apellido</th>
      <th>DNI</th>
      <th>Materias</th>
      <th>Doc Entregados</th>
    </tr>
    <tr v-for="elm in teachers" :key="elm.dni">
      <th> {{ elm.teacherName }}</th>
      <th> {{ elm.surname }}</th>
      <th> {{ elm.dni }}</th>
      <th> 
        <ul>
          <li v-for="(item, index) in elm.subjects" :key="index">{{ item }} </li>
        </ul>
      </th>
      <th v-if="elm.doc"> <p>Entregada</p> </th>
      <th v-else>No Entregada</th>
    </tr>
  </table>
    </section>
  </template>
  
  <script lang="ts" setup>
  import { Ref, ref  } from "vue";
  
  interface ITeacher{
    teacherName: string,
    surname: string,
    dni: string,
    subjects: Array<string>,
    doc: boolean
  
  }
  
  let teacher:Ref<ITeacher> = ref({
    teacherName: '',
    surname: '',
    dni: '',
    subjects: [],
    doc: false
  })
  
  let teachers:Ref<Array<ITeacher>> = ref([])
  
  let subject:Ref<string> = ref('')
  
  const handleSubject = () => {
    teacher.value.subjects.push(subject.value)
    subject.value = ''
  }
  const handAddTeacher = () => {
    teachers.value.push({
      teacherName: teacher.value.teacherName,
      surname: teacher.value.surname,
      dni: teacher.value.dni,
      subjects: teacher.value.subjects,
      doc: teacher.value.doc
    })
    teacher.value.teacherName = ""
    teacher.value.surname = ""
    teacher.value.dni = ""
    teacher.value.subjects = []
    teacher.value.doc = false
  }
  </script>
  
  <!-- ESTRUCTURA EN JS
  <script lang="ts" setup>
  import { ref  } from "vue";
  
  let teacher = ref({
    teacherName: '',
    surname: '',
    dni: '',
    subjects: [],
    docs: false
  })
  </script> -->
  
  <style>
  
  </style>
  