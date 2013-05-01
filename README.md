## Be able to query mongodb records in the given timeperiod by ObjectId
        
    var timestampToObjectId = require('timestamp-objectId');
    // timestampToObjectId = function(timestamp)
    // timestamp could be both String and actual Timestamp
    
    db.mycollection.find({
      _id: {
        $gt: timestampToObjectId('1980/05/25'),
        $lt: timestampToObjectId(1367413318476)
      }
    });
    
    ...
