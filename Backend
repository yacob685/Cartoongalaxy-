const express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');
const articleRoutes = require('./routes/articles');
const categoryRoutes = require('./routes/categories');

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect('mongodb://localhost:27017/news-website', {
  useNewUrlParser: true,
  useUnifiedTopology: true,
});

app.use('/api/articles', articleRoutes);
app.use('/api/categories', categoryRoutes);

const PORT = process.env.PORT || 5000;
app.listen(PORT, () => console.log(`Server running on port ${PORT}`));
