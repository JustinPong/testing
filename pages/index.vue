<template>
  <div class="w-full h-full flex flex-col justify-center items-center">
    <select class="mt-64" v-model="filter">
      <option :key="index" v-for="(item, index) in years" :value="item.year">
        {{ item.year }}
      </option>
    </select>
    <template v-for="(item, index) in years">
      <table v-if="filter === item.year" :key="index" class="">
        <thead>
          <tr class="w-full">
            <th>{{ item.year }}</th>
            <th>jan</th>
            <th>feb</th>
            <th>mar</th>
            <th>apr</th>
            <th>may</th>
            <th>jun</th>
            <th>jul</th>
            <th>aug</th>
            <th>sep</th>
            <th>oct</th>
            <th>nov</th>
            <th>dec</th>
          </tr>
        </thead>
        <tbody>
          <template v-for="(list, i) in item.lists">
            <tr :key="i">
              <td class="flex justify-center">{{ list.name }}</td>
              <template v-for="(month, ind) in list.months">
                <td :key="ind">
                  <input
                    class="w-[25px] flex justify-center"
                    :class="checkCSS(list.name)"
                    v-model="month.count"
                  />
                </td>
              </template>
            </tr>
          </template>
        </tbody>
      </table>
    </template>
    <button class="px-6 py-2" @click="handleExport">export</button>
    {{ newData }}
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      filter: 2010,
      newData: null,
      listItem: ["List 1", "List 2"],
      years: [
        {
          year: 2010,
          lists: [
            {
              id: "list-1",
              name: "List 1",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "",
              name: "List 2",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-3",
              name: "List 3",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-4",
              name: "List 4",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
          ],
        },
        {
          year: 2011,
          lists: [
            {
              id: "list-1",
              name: "List 1",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "",
              name: "List 2",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-3",
              name: "List 3",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-4",
              name: "List 4",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
          ],
        },
        {
          year: 2012,
          lists: [
            {
              id: "list-1",
              name: "List 1",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "",
              name: "List 2",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-3",
              name: "List 3",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-4",
              name: "List 4",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
          ],
        },
        {
          year: 2013,
          lists: [
            {
              id: "list-1",
              name: "List 1",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "",
              name: "List 2",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-3",
              name: "List 3",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
            {
              id: "list-4",
              name: "List 4",
              months: [
                {
                  key: "jan",
                  count: 0,
                },
                {
                  key: "feb",
                  count: 0,
                },
                {
                  key: "mar",
                  count: 0,
                },
                {
                  key: "apr",
                  count: 0,
                },
                {
                  key: "may",
                  count: 0,
                },
                {
                  key: "jun",
                  count: 0,
                },
                {
                  key: "jul",
                  count: 0,
                },
                {
                  key: "aug",
                  count: 0,
                },
                {
                  key: "sep",
                  count: 0,
                },
                {
                  key: "oct",
                  count: 0,
                },
                {
                  key: "nov",
                  count: 0,
                },
                {
                  key: "dec",
                  count: 0,
                },
              ],
            },
          ],
        },
      ],
    };
  },
  methods: {
    checkCSS(name) {
      if (name === "List 1" || name === "List 3") {
        return "bg-gray-100";
      } else {
        return "bg-white";
      }
    },
    handleExport() {
      const obj = {
        jan: 1,
        feb: 2,
        mar: 3,
        apr: 4,
        may: 5,
        jun: 6,
        jul: 7,
        aug: 8,
        sep: 9,
        oct: 10,
        nov: 11,
        dec: 12,
      };
      const newData = this.years.map((year) =>
        year.lists.map((list) =>
          list.months.map((month) => ({
            [list.name]: {
              year: year.year,
              month: obj[month.key],
              count: month.count,
            },
          }))
        )
      );
      const merge = newData.flat(2);
      // const filtered = merge.map(list => Object.entries(list).filter(([key]) =>
      // // key.includes(this.listItem[key])
      // this.listItem.includes(key)
      // // console.log(list)
      // ))
      // const merge2 = filtered.flat(2);
      // const filtered = merge.filter(function(e) {
      //   return this.indexOf(e) < 0;
      // },this.listItem)
      // const filtered = merge.filter((key) => !this.listItem.includes(Object.keys(key)))
      // console.log(this.listItem.includes(Object.keys(merge[10])))
      // const filtered = merge.map(function (list) {
      //   return Object.keys(list)
      //     .filter(key => this.listItem.includes(key))
      //     .reduce((obj, key) => {
      //       obj[key] = list[key];
      //       return obj;
      //     }, {});
      // });
      const self = this;
      const filtered = merge.map(function (item) {
        // console.log(self.listItem);
        return Object.keys(item)
          .filter((key) => self.listItem.includes(key))
          .reduce((obj, key) => {
            return Object.assign(obj, {
              [key]: item[key],
            });
          }, {});
      });
      const results = filtered.filter((element) => {
        if (Object.keys(element).length !== 0) {
          return true;
        }
        return false;
      });
      this.newData = results;
    },
    mounted() {
      // this.years =
    },
  },
};
</script>

<style lang="postcss" scoped>
table {
  border-collapse: collapse;
  margin: 25px 0;
  font-size: 0.9em;
  font-family: sans-serif;
  min-width: 400px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}
table thead tr,
button {
  background-color: #009879;
  color: #ffffff;
  text-align: left;
}

table th,
table td {
  padding: 12px 20px;
}

input {
  width: 30px;
}

table tbody tr {
  border-bottom: 1px solid #dddddd;
}

table tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}

table tbody tr:last-of-type {
  border-bottom: 2px solid #009879;
}

table tbody tr.active-row {
  font-weight: bold;
  color: #009879;
}
</style>