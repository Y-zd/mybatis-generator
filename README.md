自定义domain模板(增加表注释到生成domain中)的mybatis-generator生成工具
==

 使用方法:
   
   1. 只需在[mine.properties](/src/main/resources/mine.properties)文件中进行个性化配置 
   2. 运行[MyBatisGeneratorRun](/src/main/java/MyBatisGeneratorRun.java)中的main方法
   3. 生成demo如下
   
   ```java
     package com.yzd.test.domain;
     import java.io.Serializable;
     import java.util.Date;
     /**
      *
      * @author :yourName
      * @date :2019-05-16
      * 对应表 :test_table
      *
      */
     public class TestTable implements Serializable {
         
         private static final long serialVersionUID = 1L;
     
         /**
          * id
          */
         private Long id;
     
         /**
          * 创建人
          */
         private String createdBy;
     
         /**
          * 创建时间
          */
         private Date createdTime;
     
     
         public Long getId() {
             return id;
         }
     
         public void setId(Long id) {
             this.id = id;
         }
     
         public String getCreatedBy() {
             return createdBy;
         }
     
         public void setCreatedBy(String createdBy) {
             this.createdBy = createdBy == null ? null : createdBy.trim();
         }
     
         public Date getCreatedTime() {
             return createdTime;
         }
     
         public void setCreatedTime(Date createdTime) {
             this.createdTime = createdTime;
         }
     
     }
   ```
   
   ---
   TODO
      * 需要定义更多的domain样式可在[MyCommentGenerator](/src/main/java/MyCommentGenerator.java)中自行设置
   







   
   
      
        










