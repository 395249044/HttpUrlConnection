# UrlHttpUtils
��򵥵�UrlHttpUtils��װ��CallBack����ִ����UI�̡߳�֧��get����post����֧���ļ��ϴ������ء�

## ʹ�÷�����
����ܼ򵥣�ֻ������Java�ļ����������غ�Java�ļ�������������ʹ�á�

## ��װ�Ĺ����У�
###### һ���get����
###### һ���post����
###### �ϴ������ļ�(��������)
###### �ϴ�list�����ļ�
###### �ϴ�map�����ļ�
###### �ļ�����(��������)
###### ͼƬ����(ʵ����ͼƬ��ѹ��)

## ʹ��ʾ��
### GET����
	String url = "https://www.baidu.com/";
	UrlHttpUtil.get(url, new CallBackUtil.CallBackString() {
	    @Override
	    public void onFailure(int code, String errorMessage) {

	    }

	    @Override
	    public void onResponse(String response) {

	    }
	});
### POST����
    String url = "https://www.baidu.com/";
    HashMap<String, String> paramsMap = new HashMap<>();
    paramsMap.put("title","title");
    UrlHttpUtil.post(url, paramsMap, new CallBackUtil.CallBackString() {
        @Override
        public void onFailure(int code, String errorMessage) {
	
        }

        @Override
        public void onResponse(String response) {

       }
    });

### �ϴ��ļ�
        File file = new File(Environment.getExternalStorageDirectory()+"/kwwl/abc.jpg");
        HashMap<String, String> paramsMap = new HashMap<>();
        paramsMap.put("title","title");

        UrlHttpUtil.uploadFile("url", file,  "image",UrlHttpUtil.FILE_TYPE_FILE, paramsMap, new CallBackUtil.CallBackString() {
            @Override
            public void onFailure(int code, String errorMessage) {

            }

            @Override
            public void onResponse(String response) {

            }
        });

### �����ļ�
        UrlHttpUtil.downloadFile("url", new CallBackUtil.CallBackFile("fileDir","fileName") {
            @Override
            public void onFailure(int code, String errorMessage) {

            }

            @Override
            public void onProgress(float progress, long total) {
                super.onProgress(progress, total);
            }

            @Override
            public void onResponse(File response) {

            }
        });
















