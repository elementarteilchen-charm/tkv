<script setup>
    defineProps(['name', 'tankkarten', 'mautkarten'])
</script>

<template>
    <div class="mb-4">
        <div class="anbieter-kurzinfo py-2">
            <div class="font-weight-bold px-2" style="font-size: 125%;">
                {{name}}
            </div>
            <div class="d-flex">
                <div>
                    Tankkarten:
                    <span class="text-success">{{tankkarten.aktiv}}</span> / 
                    <span class="text-danger">{{tankkarten.gesperrt}}</span> / 
                    <span class="text-dark">{{tankkarten.endgueltig}}</span>
                    </div>
                <div class="ml-3">
                    Mautkarten:
                    <span class="text-success">-</span> / 
                    <span class="text-danger">-</span> / 
                    <span class="text-dark">-</span>
                </div>
            </div>
            <div class="anbieter-aktionen">
                <div class="btn btn-sm btn-primary">
                    Nettofakturierung
                </div>
                <div class="btn btn-sm btn-primary">
                    LKW&nbsp;Walter&nbsp;Vertrag
                </div>
                <div class="btn btn-sm btn-primary">
                    Anbietervertrag
                </div>
            </div>
        </div>
        
        <table class="table table-sm table-striped" style="width: 100%; font-size: 90%;">
            <thead>
                <th>&nbsp;</th>
                <th>Typ</th>
                <th>Kartennummer</th>
                <th>KundenNr</th>
                <th>&nbsp;</th>
                <th>Sponsor</th>
                <th>Gilt bis</th>
                <th>Kommentar</th>
                <th>Status</th>
                <th>Gesperrt</th>
                <th>Sperrdatum</th>
                <th>Änderung durch</th>
            </thead>
            <tbody class="">
                <tr>
                    <td><input type="checkbox"></td>
                    <td>TK </td>
                    <td>123456789012340011</td>
                    <td>12345678</td>
                    <td>Pin</td>
                    <td>10-2023</td>
                    <td>Wolfgang Wiesflecker</td>
                    <td>Ein langer Kommentar zu dieser Tankkkarte.</td>
                    <td>Erfasst</td>
                    <td>ja</td>
                    <td>3.7.2022</td>
                    <td>Leyer-Schlosser</td>
                </tr>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>TK </td>
                    <td>123456789012340011</td>
                    <td>12345678</td>
                    <td>Pin</td>
                    <td>10-2023</td>
                    <td>Wolfgang Wiesflecker</td>
                    <td>Ein langer Kommentar zu dieser Tankkkarte.</td>
                    <td>Erfasst</td>
                    <td>Nein</td>
                    <td>&nbsp;</td>
                    <td>Leyer-Schlosser</td>
                </tr>
                <tr>
                    <td><input type="checkbox"></td>
                    <td>TK </td>
                    <td>123456789012340011</td>
                    <td>12345678</td>
                    <td>Pin</td>
                    <td>10-2023</td>
                    <td>Wolfgang Wiesflecker</td>
                    <td>Ein langer Kommentar zu dieser Tankkkarte.</td>
                    <td>Erfasst</td>
                    <td>ja</td>
                    <td>3.7.2022</td>
                    <td>Leyer-Schlosser</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<style>
    div.anbieter-kurzinfo {
        display:  grid;
        grid-template-columns: 1fr 3fr 1fr;
        grid-column-gap: 0.5rem;
        align-items: center;
    }

    div.anbieter-aktionen {
        display:  grid; 
        grid-template-columns: 1fr 1fr 1fr;
        grid-column-gap: 0.25rem;
        align-items: center;
    }
</style>