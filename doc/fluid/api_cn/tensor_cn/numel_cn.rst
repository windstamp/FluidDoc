.. _cn_api_tensor_numel:

numel
-------------------------------

.. py:function:: paddle.numel(x)


该OP返回一个长度为1并且元素值为输入 ``x`` 元素个数的Tensor。

参数：
    - **x** (Tensor) - 输入Tensor，数据类型为int32，int64， float16, float32, float64, int32, int64 。

返回: 返回长度为1并且元素值为 ``x`` 元素个数的Tensor。


抛出异常：
    - ``TypeError`` - 当 ``x`` 不是Tensor或者 ``x`` 的数据类型不是bool、float16、float32、float64、int32或int64中的一个的时候

**代码示例**：

.. code-block:: python

    import paddle
        
    paddle.disable_static()
    x = paddle.full(shape=[4, 5, 7], fill_value=0, dtype='int32')
    numel = paddle.numel(x) # 140
    
