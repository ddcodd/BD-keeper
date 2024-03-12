RUN echo '#!/bin/bash
while true
do
   docker restart hungry_goodall
   sleep 7200
done' > /root/restart-container.sh
RUN chmod +x /root/restart-container.sh

# 运行这个shell脚本
CMD ["bash", "-c", "/root/restart-container.sh"]