<template>
    <div id="demo9">
        <ul>
            <li v-for="(item, index) in ['Angular', 'Vue', 'React']" :key="index">{{item}}</li>
        </ul>

        <hr>
        <ul>
            <li v-for="(item, index) in mCourses" :key="index">{{item}}</li>
        </ul>

        <hr>
        <ul>
            <li v-for="(item, index) in mCourses2" :key="index">{{item.title}} Price:{{item.price}}</li>
        </ul>

        <hr>
        <ul>
            <!-- Destructuring -->
            <li v-for="({title, price}, index) in mCourses2" :key="index">{{title}} Price:{{price}}</li>
        </ul>

        <hr>
        <input type="text" placeholder="Title" v-model="course.title"><br>
        <input type="number" placeholder="Price" v-model="course.price"><br>
        <button @click="addCourse">Submit</button>
        <ul>
            <!-- Dynamic -->
            <li v-for="(course, index) in dynamicCourses" :key="index">{{course.title}} Price:{{course.price}}
                <button @click="removeCourse(index)">X</button>
            </li>
        </ul>


    </div>
</template>
<script>
export default {
    name: "Demo9",
    methods: {
        addCourse(){
            this.dynamicCourses.push(this.course)
            this.course = {title:"", price:0}
        },
        removeCourse(index){
            this.dynamicCourses.splice(index, 1)
        }
    },
    data() {
        return {
            mCourses: ['Angular', 'Vue', 'React'],
            mCourses2: [
                {title:'iOS', price:11},
                {title:'Android', price:12},
                {title:'Flutter', price:13}
            ],
            dynamicCourses:[],
            course:{title:"", price:0},
        }
    },
}
</script>
<style>
    
</style>