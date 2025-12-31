# PDF阅读服务器 

一个支持AI助手读取和分析PDF文件的MCP服务器，提供PDF元数据提取、页面范围阅读和关键词搜索等功能。
A MCP server that supports AI assistants to read and analyze PDF files, providing functions such as PDF metadata extraction, page range reading, and keyword search## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| read_pdf | Read and extract text content from a PDF file. Returns the full text content and metadata. |
| read_pdf_page | Read a specific page or range of pages from a PDF file. |
| get_pdf_metadata | Get metadata information from a PDF file without reading all content. |
| search_pdf | Search for specific text within a PDF file. |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659716099](https://mcp.xiaobenyang.com/inspector/1777316659716099)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659716099](https://mcp.xiaobenyang.com/inspector/1777316659716099)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "PDF阅读服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659716099/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "PDF阅读服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659716099/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "PDF阅读服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659716099",
          },
          "transport": "stdio"
        }
      }
}

```
