<script>
export default {
    data() {
        return {
            records:[{
                title: 'Successfully trained',
                number: '1790',
                paragraph: 'enrolled learners',
            },
            {
                title: 'Proudly Received',
                number: '19',
                paragraph: 'countrywide awards',
            },
            {
                title: 'Firmly Established',
                number: '24',
                paragraph: 'local branches',
            },
            {
                title: 'Getting Featured on',
                number: '1090',
                paragraph: 'blog posts',
            }
        ]
        };
    }
};
</script>

<template>
    <section>
        <div class="my-container d-flex">
            <article v-for="record in records">
                <h5>
                    {{ record.title }}
                </h5>
                <span>
                    {{ record.number }}
                </span>
                <p>
                    {{ record.paragraph }}
                </p>
            </article>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

section{
    background-color: white;
}

div.my-container{
    border-left: 2px solid #f5f1ed;
}

article{
    width: calc(100% / 4);
    padding: 5rem 2.5rem;
    text-align: center;
    border-right: 2px solid #f5f1ed;

        h5{
            font-weight: 600;
            margin: 0 2rem .75rem;
        }

        span{
            font-weight: 700;
            font-size: 3rem;
            color: #20ad96;
        }

        p{
            @include uppercase-text();
            color: #8c89a2;
            font-weight: 700;
        }
}
</style>