# Avail调研

和Celestia相似，只不过在celestia的基础上增加了kzg有效性证明，不需要欺诈证明。可以看作是在Celestia上的改进版。也是设计作为一条独立的L1链。

具体来讲，就是Avail使用kzg技术来证明区块生产者的纠删编码是正确的，当区块被生产之后，轻节点（也就是轻客户端）可以立刻进行数据可用性抽样。而不是像Celestia那样当区块被生产之后，需要等待一段时间的挑战期，用来发起欺诈证明，之后才可以进行数据可用性抽样。

因此，Avail的数据可用性最终性比Celestia更快。但缺点就是，Avail比Celestia需要更多的计算来生成那些kzg证明。
