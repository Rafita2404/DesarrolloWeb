<script setup>
import { ref } from 'vue';

const fechaNacimiento = ref(null);
</script>
<template>
    <Fluid>
        <div class="flex flex-col md:flex-row gap-8">
            <div class="card flex flex-col gap-4 w-full">
                <div class="card flex flex-col gap-4">
                    <div class="font-semibold text-xl">GENERADOR DE RFC PARA UNA PERSONA</div>
                    <div class="flex flex-col gap-2">
                        <label for="name1">NOMBRE</label>
                        <InputText id="name1" type="text" />
                    </div>
                    <div>
                        <label for="name1">APELLIDO PATERNO</label>
                        <InputText id="name2" type="text" />
                    </div>
                    <div>
                        <label for="name1">APELLIDO MATERNO</label>
                        <InputText id="name3" type="text" />
                    </div>
                    <div class="flex flex-col gap-2">
                        <label for="birthdate">FECHA DE NACIMIENTO</label>
                        <Calendar id="fechaNacimiento" v-model="fechaNacimiento" dateFormat="dd/mm/yy" showIcon />
                    </div>
                    <div>
                        <label for="name1">RFC</label>
                        <InputText id="RFC" type="text" />
                    </div>
                    <div>
                        <Button label="GENERAR RFC" :fluid="false"></Button>
                    </div>
                </div>
            </div>
        </div>
    </Fluid>
</template>
