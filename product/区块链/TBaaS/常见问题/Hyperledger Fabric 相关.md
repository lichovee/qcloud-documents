### 使用 Hyperledger Fabric 如何实现隐私保护？
针对 Hyperledger Fabric，以下方式均可以不同程度地保障数据隐私性和安全性：
- 按照业务类型或者参与方对数据的访问需求，将区块链划分为若干通道，每个通道即是一条物理区块链，与其他通道的数据隔离存储和传输，数据只能被此通道的参与方访问。
- 在单个通道中，可以使用“私有数据集”特性管理数据的可访问范围。私有数据集可以定义成只允许部分参与方有权访问此数据，其他参与方只能看到此数据的摘要值。
- 参与方可以仅将数据的摘要值或者加密后的密文上链。该方式需要保证数据的访问方能够根据摘要值获取到原始数据，或者拥有对密文进行解密的密钥。
- 通过在智能合约代码中定义规则，只允许特定的角色有权限访问数据。
- 使用隐私数据集，定义数据的访问权限为特定的组织集合，也可以定义数据的生命周期。
- 数据在落盘存储时，可以使用文件系统的加密功能。在传输过程中，可以通过 TLS 进行加密传输。

默认情况下，区块链上数据的各个参与方均能直接读取到，不推荐 TBaaS 用户将任何敏感数据（例如用户身份信息、用户联系方式、资金信息等）不做任何保密处理或不做任何访问限制直接上链。如果在您的业务场景中，不确定您的业务信息是否适合上链，请 [联系我们](https://cloud.tencent.com/about/connect)。
