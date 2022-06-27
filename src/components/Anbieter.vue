<script setup>
    defineProps(['name'])
</script>

<template>
    <div class="anbieter">
        <div class="py-2 bg-light">{{name}}</div>
        
        <table>
            <thead>
                <th>Check</th>
                <th>Name</th>
                <th>Address</th>
                <th><button>Aktionen</button></th>
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
        font-size: small;
        min-height: 3rem;
    }
</style>