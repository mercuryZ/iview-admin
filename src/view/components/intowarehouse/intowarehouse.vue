<template>
  <div>
    <label style="text-align:left;font-size:16px;margin-right:5px;">搜索</label>
    <Input lable="Hello" v-model="value" placeholder="Enter something..." style="width: 300px;margin-right:5px" />
    <Button type="primary" shape="circle" icon="ios-search"></Button>
    <Button type="primary" style="margin-left:5px" @click="value1=true">快捷操作</Button>
    <Drawer
      title="Drawer"
      :closable="false"
      width="720"
      :mask-closable="false"
      v-model="value1"
    >
      <Form :model="formData" label-position="left">
        <Row :gutter="32">
          <Col span="12">
            <FormItem label="Name" label-position="left">
              <Input v-model="formData.name" placeholder="请输入姓名" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="Url" label-position="left">
              <Input v-model="formData.url" placeholder="请输入网址" >
                <span slot="prepend">Http://</span>
                <span slot="append">.com</span>
              </Input>
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="32">
          <Col span="12">
            <FormItem label="Name" label-position="top">
              <Input v-model="formData.name" placeholder="请输入姓名" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="Url" label-position="top">
              <Input v-model="formData.url" placeholder="请输入网址" >
                <span slot="prepend">Http://</span>
                <span slot="append">.com</span>
              </Input>
            </FormItem>
          </Col>
        </Row>
      </Form>
      <div class="demo-drawer-footer">
        <Button style="margin-right: 8px" @click="value1 = false">Cancel</Button>
        <Button type="primary" @click="value1 = false">Submit</Button>
      </div>
    </Drawer>

    <Table :data="tableData1" :columns="tableColumns1" style="margin-top:5px" stripe></Table>
    <div style="margin:10px;overflow:hidden">
      <div style="float:right;">
        <Page :totao="100" :current="1" @on-change="changePage"></Page>
    </div>
      </div>
  </div>
</template>

<script>
import TreeSelect from '_c/tree-select'
import { newTreeData } from '@/mock/data/tree-select'
import { getTreeSelectData } from '@/api/data'
export default {
  name: 'intowarehouse',
  components: {
    TreeSelect
  },
  data () {
    return {
      treeSelected: [112, 113],
      treeData: [],
      value1: false,
      styles: {
        height: 'calc(100% - 55px)',
        overflow: 'auto',
        paddingBottom: '53px',
        position: 'static'
      },
      formData: {
        name: '',
        url: ''
      }
    }
  },
  mounted () {
    getTreeSelectData().then(res => {
      const { data } = res
      this.treeData = data
    })
  },
  methods: {
    changeTreeSelectData () {
      this.treeSelected = [111, 114]
    },
    changeTreeData () {
      this.treeData = newTreeData
      // this.treeSelected = [];
    },
    handleTreeSelectChange (list) {
      // console.log('=-========', list);
    },
    handleTreeSelectExpand (item) {
      // console.log('toggle expand', item);
    },
    handleTreeSelectCheckChange (selectedArray, item) {
      // console.log(selectedArray, item);
    },
    handleTreeSelectClick (selectArray, item) {
      // console.log(selectArray, item);
    },
    loadData (item, callback) {
      setTimeout(() => {
        let data = [
          {
            id: 111,
            title: '1-1-1'
          },
          {
            id: 112,
            title: '1-1-2'
          },
          {
            id: 113,
            title: '1-1-3'
          },
          {
            id: 114,
            title: '1-1-4'
          }
        ]
        callback(data)
      }, 1000)
    }
  }
}
</script>

<style>
    .demo-drawer-footer{
        width: 100%;
        position: absolute;
        bottom: 0;
        left: 0;
        border-top: 1px solid #e8e8e8;
        padding: 10px 16px;
        text-align: right;
        background: #fff;
    }
</style>
