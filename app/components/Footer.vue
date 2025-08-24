<template>
    <div class="bg-gray-100 dark:bg-gray-800 py-4">
        <div class="prose mx-auto dark:prose-invert p-4 md:text-lg opacity-60">

            <div class="flex-col md:flex-row flex justify-between border-b-2 border-b-gray-300">
                <div>
                    <p class="text-sm text-left">
                        朱玺霖 | Xilin <br />
                        Incoming Ph.D Student <br />
                        Department of Computing and Information Sciences Ph.D. <br />
                        Rochester Institute of Technology <br />
                    </p>
                </div>

                <div>
                    <p class="text-sm md:text-right [&_br]:hidden [&_br]:md:inline">
                        <a href="mailto:alex.xilin.zhu@gmail.com">E-Mail</a> <br />
                        <!--
                        <a href="https://github.com/YiqinZhao">GitHub</a> <br />
                        <a href="https://bsky.app/profile/yiqinzhao.bsky.social">Bluesky</a> <br />
                        -->
                    </p>
                </div>
            </div>


            <div class="text-gray-500 dark:text-gray-400 mx-auto text-sm">
                <p>
                    © <a href="https://xilinzhu.me">Xilin Zhu</a> {{ year }}. Last updated: {{ datetime }}.
                    Use my website <a class="underline" href="https://github.com/YiqinZhao/yiqinzhao.me-source">template made by Yiqin Zhao</a>.
                </p>
            </div>

        </div>

    </div>
</template>

<script setup>
import lastUpdated from '~/static/lastUpdated';

const lastUpdatedTime = new Date(lastUpdated.timestamp)
const year = lastUpdatedTime.getFullYear()
const datetime = lastUpdatedTime.toLocaleDateString()
</script>
