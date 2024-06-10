<script>
import { Loader } from '@googlemaps/js-api-loader';


export default {
    name: 'GoogleMap',
    data() {
        return {
            map: null,
            loader: null,
        };
    },

    mounted() {
        this.loader = new Loader({
            apiKey: 'AIzaSyAekxfjpmwK1GBkaGm7oy7d90AnNK9ZDpw',
            version: 'weekly',
        });

        this.loader.load().then(() => {
            this.map = new google.maps.Map(this.$refs.mapContainer, {
                center: { lat: -7.1126525596576595, lng:  -34.85401234417924 },
                zoom: 15,
            });

      // Add marker
        const marker = new google.maps.Marker({
            position: { lat: -7.1126525596576595, lng:  -34.85401234417924 },
            map: this.map,
            title: 'Regular Cand',
        });
        });
    },
};
</script>

<template>
    <section><!--LOCALIZACAO-->
        <div ref="mapContainer" style="height: 400px;"></div>
    </section>
</template>

<style scoped>
</style>