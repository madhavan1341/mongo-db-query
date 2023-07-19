# mongo-db-query

1.db.products.find({})
2.db.products.find({
  product_price: { $gte: 400, $lte: 800 }
})
3.db.products.find({
  product_price: { $not: { $gte: 400, $lte: 600 } }
})
4.db.products.find({
  product_price: { $gt: 500 }
}).limit(4)
5.db.products.find({}, { product_name: 1, product_material: 1, _id: 0 })
6.db.products.findOne({ id: "10" })
7.db.products.findOne({ id: "10" }, { product_name: 1, product_material: 1, _id: 0 })
8.db.products.find({ product_material: { $regex: /soft/i } })
9.db.products.find({
  product_color: "indigo",
  product_price: 492.00
})
10.db.products.deleteMany({
    product_price: product.product_price,
    _id: { $ne: product._id }
  })
