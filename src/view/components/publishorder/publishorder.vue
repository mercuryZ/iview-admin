<template>
  <div>
    <label style="text-align:left;font-size:16px;margin-right:5px;">搜索</label>
    <Input v-model="value" placeholder="Enter something..." style="width: 300px;margin-right:5px" />
    <Button type="primary" shape="circle" icon="ios-search"></Button>
    <Button type="primary" style="margin-left:5px" @click="value1=true">快捷操作</Button>
    <Drawer
      title="Drawer"
      closable="false"
      width="1080"
      :mask-closable="false"
      v-model="value1"
      scrollable="true"
    >
      <Form :model="formData" label-position="left">
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="预订单编号">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="ERP订单编号">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="订单录入类型" label-position="left">
              <Input label="Hello" v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="订单类型" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="订单类别" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="是否全额增送订单" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="费用类型" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="物资类型" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="供货单流水号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="采购协同编号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="合同主体代码" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="合同主体名称" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="ERP导入状态" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="订单头同步合同系统状态" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="合同名称" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="合同编码" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="框架协议编号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="框架协议名称" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="是否可抵扣" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="税率（6%）" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="不含税金额（元）" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="税金（元）" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="采购订单币种" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="采购订单总价（元）" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="供应商名称" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="ERP供应商编号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="纳税资质" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="ERP供应商地点" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="供应商开户银行" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="供应商银行编号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="供应商联系人" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="供应商联系人电话" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="供应商联系人传真" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="供应商联系人Email" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="卖方销售订单号" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="供应商地址" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
        <Row :gutter="24">
          <Col span="12">
            <FormItem label="订单创建时间" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
          <Col span="12">
            <FormItem label="订单生成时间" label-position="top">
              <Input v-model="formData.name" />
            </FormItem>
          </Col>
        </Row>
      </Form>
      <div class="demo-drawer-footer">
        <Button style="margin-right: 8px" @click="value1=false">Cancel</Button>
        <Button type="primary" @click="value1=false">Submit</Button>
      </div>
    </Drawer>
    <Table :data="tableData1" :columns="tableColumns1" stripe style="margin-top:10px"></Table>
    <div style="margin: 10px;overflow: hidden">
      <div style="float: right;">
        <Page :total="100" :current="1" @on-change="changePage"></Page>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'publishorder',
  data () {
    return {
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
      },
      tableData1: this.mockTableData1(),
      tableColumns1: [
        {
          title: 'Name',
          key: 'name'
        },
        {
          title: 'Status',
          key: 'status',
          render: (h, params) => {
            const row = params.row
            const color = row.status === 1 ? 'primary' : row.status === 2 ? 'success' : 'error'
            const text = row.status === 1 ? 'Working' : row.status === 2 ? 'Success' : 'Fail'

            return h('Tag', {
              props: {
                type: 'dot',
                color: color
              }
            }, text)
          }
        },
        {
          title: 'Portrayal',
          key: 'portrayal',
          render: (h, params) => {
            return h('Poptip', {
              props: {
                trigger: 'hover',
                title: params.row.portrayal.length + 'portrayals',
                placement: 'bottom'
              }
            }, [
              h('Tag', params.row.portrayal.length),
              h('div', {
                slot: 'content'
              }, [
                h('ul', this.tableData1[params.index].portrayal.map(item => {
                  return h('li', {
                    style: {
                      textAlign: 'center',
                      padding: '4px'
                    }
                  }, item)
                }))
              ])
            ])
          }
        },
        {
          title: 'People',
          key: 'people',
          render: (h, params) => {
            return h('Poptip', {
              props: {
                trigger: 'hover',
                title: params.row.people.length + 'customers',
                placement: 'bottom'
              }
            }, [
              h('Tag', params.row.people.length),
              h('div', {
                slot: 'content'
              }, [
                h('ul', this.tableData1[params.index].people.map(item => {
                  return h('li', {
                    style: {
                      textAlign: 'center',
                      padding: '4px'
                    }
                  }, item.n + '：' + item.c + 'People')
                }))
              ])
            ])
          }
        },
        {
          title: 'Sampling Time',
          key: 'time',
          render: (h, params) => {
            return h('div', 'Almost' + params.row.time + 'days')
          }
        },
        {
          title: 'Updated Time',
          key: 'update',
          render: (h, params) => {
            return h('div', this.formatDate(this.tableData1[params.index].update))
          }
        }
      ]
    }
  },
  methods: {
    mockTableData1 () {
      let data = []
      for (let i = 0; i < 10; i++) {
        data.push({
          name: 'Business' + Math.floor(Math.random() * 100 + 1),
          status: Math.floor(Math.random() * 3 + 1),
          portrayal: ['City', 'People', 'Cost', 'Life', 'Entertainment'],
          people: [
            {
              n: 'People' + Math.floor(Math.random() * 100 + 1),
              c: Math.floor(Math.random() * 1000000 + 100000)
            },
            {
              n: 'People' + Math.floor(Math.random() * 100 + 1),
              c: Math.floor(Math.random() * 1000000 + 100000)
            },
            {
              n: 'People' + Math.floor(Math.random() * 100 + 1),
              c: Math.floor(Math.random() * 1000000 + 100000)
            }
          ],
          time: Math.floor(Math.random() * 7 + 1),
          update: new Date()
        })
      }
      return data
    },
    formatDate (date) {
      const y = date.getFullYear()
      let m = date.getMonth() + 1
      m = m < 10 ? '0' + m : m
      let d = date.getDate()
      d = d < 10 ? ('0' + d) : d
      return y + '-' + m + '-' + d
    },
    changePage () {
      // The simulated data is changed directly here, and the actual usage scenario should fetch the data from the server
      this.tableData1 = this.mockTableData1()
    }
  }
}
</script>
<style>
.demo-drawer-footer{
  width: 100%;
  position: relative;
  bottom: 0;
  left: 0;
  border-top: 1px solid #e8e8e8;
  padding: 10px 16px;
  text-align: right;
  background: #fff;
}
</style>
