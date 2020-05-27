<template>

    <div class="container">
        <li v-for="provider in providers" :key="provider.name">
            <span>{{ provider.name }}</span>
            <span>{{ provider.address }}</span>
            <span>{{ provider.phone }}</span>
        </li>
    <table>
        <thead>
            <tr>
                <th colspan="3">Providers</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><input type="text" id="pname"></td>
                <td><input type="text" id="paddress"></td>
                <td><input type="text" id="pphone"></td>
            </tr>
        </tbody>
    </table>
    </div>
</template>

when will we start to demo

<script>

   export default{
    data: function() {
        return {
            providers: [
                {
                    id: 1,
                    name: 'Steven',
                    address: '12 paper',
                    phone: '555.555.5555'
                },
                                {
                    id: 2,
                    name: 'Jeo',
                    address: '42 towel',
                    phone: '333.555.5555'
                },
                                {
                    id: 1,
                    name: 'Scott',
                    address: 'Lake St',
                    phone: '444.555.5555'
                },
                                {
                    id: 1,
                    name: 'Doctor Strange',
                    address: 'New York',
                    phone: '222.555.5555'
                },
            ]
        };
    }
   }

</script>

<style>
    span {
        padding: 3px;
    }
</style>
 