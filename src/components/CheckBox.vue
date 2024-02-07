<template>
<h2>Check Box</h2>
<label for="">Technology Languages :</label><br /><br />
<label for="java">Java</label>
<input type="checkbox" name="" id="java" value="Java" v-model="technology" />
<br /><br />
<label for="php">PHP</label>
<input type="checkbox" name="" id="php" value="PHP" v-model="technology" />
<br /><br /><label for="NODE">Node</label>
<input type="checkbox" name="" id="NODE" value="Node" v-model="technology" />
<br /><br />
<h2>Technology {{ technology }}</h2>
<br /><br />

<h2>Who I Am?</h2>
<br />

<label for="student">Student</label>
<input type="radio" name="who" id="student" value="Student" v-model="who" />
<br /><br />
<label for="engineer">Engineer</label>
<input type="radio" name="who" id="engineer" value="Engineer" v-model="who" />
<br /><br />
<h2>I am :{{ who }}</h2>

<h2 v-if="show">Show If Condition</h2>
<h3 v-else>Show Else Condition</h3>
<button v-on:click="show = !show">Toggle</button>

<ul>
    <li v-for="item in language" :key="item">
        {{ item }}
    </li>
</ul>

<ul>
    <li v-for="item in user" :key="item.name">
        Name is : {{ item.name }} and Email is : {{ item.email }}
    </li>
</ul>
</template>

<script>
export default {
    name: "CheckBox",
    data() {
        return {
            technology: [],
            who: null,
            show: true,
            language: ["bangla", "english", "hindi"],
            user: [{
                    name: "Mynul",
                    email: "mynul@gmail.com",
                },
                {
                    name: "Mynul1",
                    email: "mynul1@gmail.com",
                },
                {
                    name: "Mynul2",
                    email: "mynul2@gmail.com",
                },
            ],
        };
    },
};
</script>
