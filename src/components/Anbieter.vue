<script setup>
    defineProps(['name'])
</script>

<template>
    <div class="anbieter">
        <div class="py-2 bg-info">{{name}}</div>
        
        <table style="width: 100%;">
            <thead>
                <th>Check</th>
                <th>Name</th>
                <th>Address</th>
                <th></th>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>Team-Sponsor Nachname</td>
                    <td>2345 Brunn am Gebirge</td>
                    <td>34592974705767</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<style>
    div.anbieter {
        /*display:  grid;
        grid-template-columns: 1fr;*/
        min-height: 3rem;
    }
</style>